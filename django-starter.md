# Django Starter

I assume you're working in Command Prompt on a windows machine. **$** indicates the prompt path.

It's a good practice to create a virtual environment before you work on your project. 

#### 1. Install Virtualenv
```
$ pip install virtualenv
```

#### 2. Create a virutalenv instance
```
$ virtualenv your_environment_name
```

#### 3. Activate the environment
```
$ cd your_environment_name/

dir_path\your_environment_name> $ Scripts\activate
```

#### 4. Install Django 1.11 in the Virtual Environment
```
(your_environment_name) $ pip install django==1.11
```

#### 5. Start a Django Project
```
(your_environment_name) $ django-admin startproject your_project_name
```

#### 6. Navigate to project folder
```
(your_environment_name) $ cd your_project_name
(your_environment_name) $ dir
|-- manage.py
|-- myproject/
      |-- settings.py
      |-- urls.py
      |-- wsgi.py
      |-- __init__.py
 ```

#### 7. Freeze requirements.txt to keep track of dependencies
```
(your_environment_name) $ pip freeze >requirements.txt
(your_environment_name) $ dir
|-- manage.py
|-- myproject/
|-- requirements.txt

(your_environment_name) $ more requirements.txt
Django==1.11
pytz==2018.3
```

