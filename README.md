# Rauan.github.io
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="description" content="Лучший магазин книг">
    <meta name="keywords" content="книги, интернет-магазин, литература">
    <meta name="author" content="Kaliev_Rauan">
    <title>Интернет-магазин книг</title>
    <link rel="stylesheet" href="styles.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/toastr.js/latest/toastr.min.css">
    <script src="https://cdn.jsdelivr.net/npm/vue@2"></script>
    <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/toastr.js/latest/toastr.min.js"></script>
</head>
<body>
    <video autoplay muted loop id="bg-video">
        <source src="88.mp4" type="video/mp4">
    </video>

    <div id="app">
        <div id="content" class="animate__animated animate__fadeIn">
            <h1 align="center">Добро пожаловать в наш магазин электронных книг</h1>

            <div id="intro" class="styled-div">
                <img src="12.png" alt="Магазин книг" class="float-img">
                <p>Этот интернет-магазин предлагает широкий ассортимент электронных книг на любой вкус. Вы найдете здесь произведения классиков и современных авторов, а также учебную литературу и научные издания.</p>
            </div>

            <h2 class="center-text">Книжный магазин</h2>

            <h3 align="center">Каталог книг</h3>
            <div id="book-list" align="center">
                <div v-for="book in books" :key="book.title">
                    <p>
                        <a :href="book.link" class="book-link"><cite>{{ book.title }}</cite></a> - <span class="price">{{ book.price }}тг</span>
                    </p>
                </div>
            </div>
            <div align="center">
                <button @click="sortBooksByPrice">Отсортировать</button>
            </div>

            <h3 align="center">Добавить новую книгу</h3>
            <div align="center">
                <input v-model="newBook.title" placeholder="Название книги">
                <input v-model="newBook.price" placeholder="Цена">
                <input v-model="newBook.link" placeholder="Ссылка">
                <button @click="addBook">Добавить книгу</button>
            </div>

            <h3 align="center">Удалить последнюю книгу</h3>
            <div align="center">
                <button @click="removeLastBook">Удалить последнюю книгу</button>
            </div>

            <h3 align="center" id="contacts">Контакты</h3>
            <ul>
                <li><strong>Наш адрес:</strong> г.Усть-каменогорск, ул.Нагорная, 3а</li>
                <li><strong>Телефон:</strong> +7 777 709 3111</li>
                <li><strong>Email:</strong> <a href="mailto:rayancaliev@gmail.com">rayancaliev@gmail.com</a></li>
            </ul>

            <h3 align="center" id="delivery">Информация о доставке</h3>
            <table id="delivery-options" align="center" border="1" width="80%" class="styled-table">
                <caption><strong>Варианты доставки</strong></caption>
                <tr>
                    <th>Вариант доставки</th>
                    <th>Стоимость</th>
                    <th>Срок доставки</th>
                </tr>
                <tr>
                    <td>Курьерская доставка</td>
                    <td>1000тг</td>
                    <td>1-2 дня</td>
                </tr>
                <tr>
                    <td>Почтовая доставка</td>
                    <td>500тг</td>
                    <td>3-5 дней</td>
                </tr>
                <tr>
                    <td>Самовывоз</td>
                    <td>Бесплатно</td>
                    <td>В день заказа</td>
                </tr>
            </table>
            <div align="center">
                <button @click="sortDeliveryOptions">Отсортировать</button>
            </div>

            <h3 align="center">Ссылки</h3>
            <div align="center">
                <p><a href="#catalog">Каталог</a></p>
                <p><a href="#contacts">Контакты</a></p>
                <p><a href="#delivery">О доставке</a></p>
            </div>

            <h3 align="center">Наши преимущества</h3>
            <div align="center">
                <ol style="list-style-position: inside;">
                    <li>Широкий ассортимент книг</li>
                    <li>Быстрая доставка</li>
                    <li>Низкие цены</li>
                </ol>
            </div>

            <h3 align="center">Ссылка чтобы сделать заказ</h3>
            <p align="center">
                <a href="https://forms.gle/3fkt8U4zFCGnmhXC9" target="_blank">Оформите заказ</a>
            </p>
            
            <h3 align="center" style="color: white;">Обратная связь</h3>
            <div align="center">
                <form action="https://formspree.io/f/mqazvgjq" method="POST" style="color: white;">
                    <label for="name" style="color: white;">Имя:</label><br>
                    <input type="text" id="name" name="name" required><br><br>

                    <label for="email" style="color: white;">Электронная почта:</label><br>
                    <input type="email" id="email" name="email" required><br><br>

                    <label for="message" style="color: white;">Сообщение:</label><br>
                    <textarea id="message" name="message" rows="4" required></textarea><br><br>

                    <button type="submit">Отправить</button>
                </form>
            </div>

            <h3 align="center">jQuery Демонстрация</h3>
            <div align="center">
                <button id="jquery-button">Кнопка</button>
                <button id="jquery-css-button">Изменить стиль</button>
                <button id="jquery-html-button">Изменить HTML</button>
                <button id="jquery-append-button">Добавить элемент</button>
            </div>
        </div>
    </div>

    <script src="script.js"></script>
</body>
</html>
