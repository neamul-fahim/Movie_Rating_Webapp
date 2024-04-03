# Movie-Rating-Webapp

--------------------------------------------------MY CV------------------------------------------

https://drive.google.com/file/d/1N9qlN6tBEXshT-HFGH28GCWc-6NzxERC/view?usp=sharing

--------------------------------------------------MY CV------------------------------------------

# Create a Virtual Envirment

1. pip install virtualenv
2. virtualenv .venv
3. .venv/Scripts/activate

# Install packages

1. pip install -r requirements.txt
2. python manage.py makemigrations
3. python manage.py migrate

# Runserver

1. python manage.py runserver

I was unable to manage a cloud database. Please consider the situation.

# Features

1. User can Signup and Login. Implemented Custom User model using "AbstractBaseUser". Implemented Token Authentication. Used Django RestFramework.
2. User can add a movie.
3. User can view a list of all movies.
4. User can rate a movie also can see Movie details and average rating while rating. As the user submits rating the average rating will be reflected on the screen instantly.
5. User can search up a specific movie and see it’s details along with the average rating of a movie. Search will match substring of the movies name and show all the matches of movie information available.

# Problems i faced and Solved

1. When we use custom user model and try to save the user through serializer the custome user's create_user() method doesn't get called so we have to override the serializers create() method to call create_user() method.
2. When we use custom user model and try to create user using django admin panel, the user password doesn't get hashed. so we neet to make some changes to the UserAdmin in the admin.py file and register it to the admin panel with our custom user model. This problem occurs because django's admin panel doesn't have a clear idea of our custom user model.
3. We can't provide same name for a model and it's attribute like: model name "Rating" and it's attribute 'rating'. Eventhough the model name is in capital letter it will clash.
