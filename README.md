> ## Rest API для проекта Yatube
> ### Интерфейс для обмена данными с социальной сетью Yatube с использзованием API.
> Проект позволяет:
> - получать список публикаций или конкретную публикацию
> - создавать, обновлять или удалять публикации авторами
> - получать список комментариев или конкретный комментарий
> - добавлять, обновлять или удалять комментарий автороами
> - получать спосок сообществ или инофрмации о сообществе
> - подписываться на авторов
> - получать токена аутентификации 

### Технологии
* Django==2.2.16
* djangorestframework==3.12.4
* djangorestframework-simplejwt==4.7.2

## Как запустить проект:
Клонировать репозиторий и перейти в него в командной строке:

```
git clone https://github.com/kazhuha/api_final_yatube.git
```
```
cd api_final_yatube
```
Создать и активировать виртуальное окружение:
```
python -m venv venv
```
```
source venv/bin/activate
```
Установить зависимости из файла requirements.txt:
```
pip install -r requirements.txt
```
Выполнить миграции:
```
python3 manage.py migrate
```
Запустить проект:
```
python3 manage.py runserver
```

## Примеры запросов:
| Действие  | Запрос |Тип запроса |
| ------------- | ------------- |------------- |
| Получение публикаций  | http://127.0.0.1:8000/api/v1/posts/ | GET |
| Создание публикаций | http://127.0.0.1:8000/api/v1/posts/ | POST |
| Получение публикации | http://127.0.0.1:8000/api/v1/posts/{id}/ | GET |
| Обновление, удаление публикации | http://127.0.0.1:8000/api/v1/posts/{id}/ | PUT, PATCH, DEL |
| Получение комментариев | http://127.0.0.1:8000/api/v1/posts/{post_id}/comments/ | GET |
| Добавление комментария | http://127.0.0.1:8000/api/v1/posts/{post_id}/comments/ | POST |
| Получение комментария | http://127.0.0.1:8000/api/v1/posts/{post_id}/comments/{id}/ | GET |
| Обновление, удаление комментария | http://127.0.0.1:8000/api/v1/posts/{post_id}/comments/{id}/ | PUT, PATCH, DEL |
| Список сообществ | http://127.0.0.1:8000/api/v1/groups/ | GET |
| Информация о сообществе | http://127.0.0.1:8000/api/v1/groups/{id}/ | GET |
| Подписки | http://127.0.0.1:8000/api/v1/follow/ | GET |
| Подписка на автора | http://127.0.0.1:8000/api/v1/follow/ | POST |

### Автор
Кожушкевич Александр 