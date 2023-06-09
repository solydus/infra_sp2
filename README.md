# api_yamdb
Проект YaMDb собирает отзывы пользователей на произведения. Сами произведения в YaMDb не хранятся, здесь нельзя посмотреть фильм или послушать музыку.
Произведения делятся на категории, такие как «Книги», «Фильмы», «Музыка». Например, в категории «Книги» могут быть произведения «Винни-Пух и все-все-все» и «Марсианские хроники», а в категории «Музыка» — песня «Давеча» группы «Жуки» и вторая сюита Баха. Список категорий может быть расширен (например, можно добавить категорию «Изобразительное искусство» или «Ювелирка»). 

<h2>Стек технологий</h2>
проект написан на Python с использованием Django REST Framework
библиотека Simple JWT - работа с JWT-токеном
библиотека django-filter - фильтрация запросов
база данных - SQLite3
система управления версиями - git

<h2>Для запуска проекта</h2> выполните следующие команды:

python manage.py migrate

python manage.py createsuperuser

python3 -m venv venv

. venv/bin/activate

pip install -r requirements.txt

<h2>Ресурсы API YaMDb</h2>
Ресурс auth: аутентификация.
Ресурс users: пользователи.
Ресурс titles: произведения, к которым пишут отзывы (определённый фильм, книга или песенка).
Ресурс categories: категории (типы) произведений («Фильмы», «Книги», «Музыка»). Одно произведение может быть привязано только к одной категории.
Ресурс genres: жанры произведений. Одно произведение может быть привязано к нескольким жанрам.
Ресурс reviews: отзывы на произведения. Отзыв привязан к определённому произведению.
Ресурс comments: комментарии к отзывам. Комментарий привязан к определённому отзыву.
Самостоятельная регистрация новых пользователей
Пользователь отправляет POST-запрос с параметрами email и username на эндпоинт /api/v1/auth/signup/.
Сервис YaMDB отправляет письмо с кодом подтверждения (confirmation_code) на указанный адрес email.
Пользователь отправляет POST-запрос с параметрами username и confirmation_code на эндпоинт /api/v1/auth/token/, в ответе на запрос ему приходит token (JWT-токен).

<h3>Авторы:</h3>
https://github.com/solydus<br>
https://github.com/Tatiana-Akhmadullina<br>
https://github.com/RuslanPetilava
