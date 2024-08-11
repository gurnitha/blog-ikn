# django5-blog
Membuat aplikasi Blog: Mengklon Medium Menggunakan Django versi 5


## 1. SETUP

#### 1. Membuat lingkungan virtual

        modified:   README.md
        new file:   venv312507/Scripts/Activate.ps1
        new file:   venv312507/Scripts/activate
        new file:   venv312507/Scripts/activate.bat
        new file:   venv312507/Scripts/deactivate.bat
        new file:   venv312507/Scripts/pip.exe
        new file:   venv312507/Scripts/pip3.12.exe
        new file:   venv312507/Scripts/pip3.exe
        new file:   venv312507/Scripts/python.exe
        new file:   venv312507/Scripts/pythonw.exe
        new file:   venv312507/pyvenv.cfg

#### 2. Mengaktifkan lingkungan virtual

        λ venv312507\Scripts\activate.bat

        C:\Users\ING\Desktop\django5-blog(main -> origin)
        (venv312507) λ

        modified:   .gitignore
        modified:   README.md

#### 3. Menginstal Django versi 5.0.7

        (venv312507) λ pip install django==5.0.7
        Collecting django==5.0.7
          ...
        Successfully installed asgiref-3.8.1 django-5.0.7 sqlparse-0.5.1 tzdata-2024.1

        [notice] A new release of pip is available: 23.2.1 -> 24.2
        [notice] To update, run: python.exe -m pip install --upgrade pip

        modified:   README.md


## 2. PROYEK DJANGO

#### 1. Menginisiasi proyek

        modified:   README.md
        new file:   config/config/__init__.py
        new file:   config/config/asgi.py
        new file:   config/config/settings.py
        new file:   config/config/urls.py
        new file:   config/config/wsgi.py
        new file:   config/manage.py

#### 2. Menjalankan server django

        (venv312507) λ python manage.py runserver
        modified:   README.md

#### 3. Mengaktifkan default app django

        (venv312507) λ python manage.py migrate
        modified:   README.md

#### 4. Membuat superuser

        modified:   README.md


## 3. SETTING

#### 1. Memodifikasi struktur file proyek

        modified:   README.md
        renamed:    config/config/__init__.py -> config/__init__.py
        renamed:    config/config/asgi.py -> config/asgi.py
        renamed:    config/config/settings.py -> config/settings.py
        renamed:    config/config/urls.py -> config/urls.py
        renamed:    config/config/wsgi.py -> config/wsgi.py
        renamed:    config/manage.py -> manage.py
        deleted:    venv312507/Scripts/Activate.ps1
        deleted:    venv312507/Scripts/activate
        deleted:    venv312507/Scripts/activate.bat
        deleted:    venv312507/Scripts/deactivate.bat
        deleted:    venv312507/Scripts/pip.exe
        deleted:    venv312507/Scripts/pip3.12.exe
        deleted:    venv312507/Scripts/pip3.exe
        deleted:    venv312507/Scripts/python.exe
        deleted:    venv312507/Scripts/pythonw.exe
        deleted:    venv312507/pyvenv.cfg

#### 2. Seting bahasa dan waktu

        modified:   README.md
        modified:   config/settings.py


## 4. DATABASE

#### 1. Membuat MySQL database

        E:\_WORKSPACE\laragon\bin\cmder
        λ mysql -u root
        Welcome to the MySQL monitor.  Commands end with ; or \g.
        Your MySQL connection id is 8
        Server version: 8.0.30 MySQL Community Server - GPL

        Copyright (c) 2000, 2022, Oracle and/or its affiliates.

        Oracle is a registered trademark of Oracle Corporation and/or its
        affiliates. Other names may be trademarks of their respective
        owners.

        Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

        mysql> CREATE DATABASE django5_blog;
        Query OK, 1 row affected (0.10 sec)

        mysql> SHOW databases;
        +---------------------------------------------------------+
        | Database                                                |
        +---------------------------------------------------------+
        ...
        | django5_blog                                            |
        ...
        +---------------------------------------------------------+
        120 rows in set (0.09 sec)

#### 2. Menghubungkan proyek dengan database

        modified:   README.md
        modified:   config/settings.py

#### 3. Menginstal MySQL driver (mysqlclient)

        (venv312507) λ pip install mysqlclient

#### 4. Meng-upgrade pip

        (venv312507) λ python.exe -m pip install --upgrade pip
        Requirement already satisfied: pip in 
        ...
        Successfully installed pip-24.2