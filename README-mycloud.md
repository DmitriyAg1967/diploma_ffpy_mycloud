# mycloud
Мой дипломный проект  


### Запуск локально
___
1. Установка зависимостей
```
pip install -r requirements.txt
```
2. Проверьте файл конфигурации, измените конфигурацию почтового ящика и базы данных
```
# mycloud/settings.py

EMAIL_HOST = 'localhost'
EMAIL_PORT = '25'
EMAIL_HOST_USER = ''
EMAIL_HOST_PASSWORD = ''
EMAIL_USE_TLS = False
DEFAULT_FROM_EMAIL = 'webmaster@localhost'


DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql_psycopg2',
        'NAME': 'cloud',
        'HOST': '127.0.0.1',
        'PORT': '5432',
        'USER': 'postgres',
        'PASSWORD': '********',
    }
} }
}
```
3. Перенос базы данных
```
python manage.py migrate

```
4Создайте суперпользователя
```
python manage.py createsuperuser
```
5Запустите локальный сервер
```
python manage.py runserver
```
### Скриншот страницы
___ 
Панель администратора

![screen shot](images/admin.jpeg) 

Вход или Регистрация  

![screen shot](images/auth.png)  

Список файлов  

![screen shot](images/main.jpeg)

Личная информация 

![screen shot](images/info.jpeg)  

