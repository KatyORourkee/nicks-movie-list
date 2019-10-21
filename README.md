# nicks-movie-list
My husband finally cancelled his Netflix DVD subscription that he's had for years and years. Now that it's gone, he misses a decision-free way of getting a new movie to watch. This app is meant to take a list of movies to watch and suggest one, forcing him to watch that one before a new one can be suggested. Trust me, he will like it!

# Steps used to create this project (Windows):
1. In folder, create virtual environment
> python -m venv .env

2. Activate the virtual environment by running the activate script
> /.env/scripts/activate 

3. Install django 
> pip install django 

4. Add gitignore file so there aren't so many changes (the install of django)

5. Create the project
> django-admin startproject nicksmovielist .
The dot at the end of this command indicates not to create an extra folder, putting the management app right inside the folder I already have created. I did not include the dot in my command so there is an extra nested folder. 

6. Tested that the project was created successfully by running the server and navigating to the URL.
> cd nicksmovielist
> python manage.py runserver

7. Create the first django application 
> python manage.py startapp movies

# Route to the new app
1. In the management app urls.py, add a URL pattern for 'movies' to route to movies/urls.py

2. In movies/urls.py, add a URL pattern for '' to tell the app which view to go to. 

3. Define that new view in movies/views.py, telling it which template to go to.

4. In the movies app, create a template/movies/index.html (or any html file name you provided to the view) with basic HTML in it. The nested folder structure is to allow the app to easily find the right index.html if there is another app with an index.html. It will know to go to movies/index.html once all of the templates folders end up in the same place.

5. In settings.py, register the app and the template URL. 