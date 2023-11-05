# Tool Learning Log

Tool: **Django**

Project: **X**

---

**10/23/23**:
* I first went on the [Django website](https://www.w3schools.com/django/index.php) and looked at the list of tutorials the webiste has on Django. Then I saw the word "URL" and "APP".
* I wanted to create a slide card app that students can use to review their vocabulary, and study for exams. Students can choose to add onto their list of flashcards, and make quizzes for studying.
* My tool is a Python framework that lets us create apps and or webistes.
* AIt follows the MTV (Model View Template)

**10/24/23**:

**Model**: 
* the data is delivered as a object relational mapping (ORM), which is a technique designed to make it easier to work with databases.
* Using ORM would make it easier to communicate with databases without having to write complex SQL statements.
* most common way to extract data from a database is SQL. 
* The models are usually located in a file called `models.py`
  
**10/25/23**:

**View**:
* a function or method that takes http requests as arguments, imports the relevant model(s), and finds out what data to send to the template, and returns the final result.
* The views are usually located in a file called `views.py`
  
**10/27/23**:

**Template**:
* uses HTML layouts with logic, example shown below:
  ```html
  <h1>My Homepage</h1>

  <p>My name is {{ firstname }}.</p>
  ```
* The templates of an application is located in a folder named `templates`

**10/30/23**

**URLS**
* Used to navigate around different pages inside the website.
* When a user requests a URL, Django will bring you to the designated URL.
* The file is called `urls.py`

**11/1/23**

Since I needed to learn more about making an app for my freedom project, I look at the [Django Create App](https://www.w3schools.com/django/django_create_app.php) part of the website. I ama very stressed out right now, becasue the website doesn't say much about how to build an app. But it did tell me that I would need a start app name and a folder to navigate where I would want to locate the information. 
```django
py manage.py startapp members
```
Django will creates a folder named `members` in my project, with this content:
```django
my_tennis_club
    manage.py
    my_tennis_club/
    members/
        migrations/
            __init__.py
        __init__.py
        admin.py
        apps.py
        models.py
        tests.py
        views.py
```
These are all the file with specific meanings. 

**11/2/23**

I realized that I didnt know where to code my project yet, and since the tool Django is python. I found thet replit can code Python and since Django is part of Python, we will be able to use [replit](https://blog.replit.com/deploying-django). 
* Authentication and authorization have been previously incorporated into Django, which means you can focus on writing your app because the basic web development functionality has already been done.
* Replit also allows for real-time collaboration. You can access Replit on any platform that has an active internet connection, and you can edit your code and connect with other developers anytime and anywhere.


X/X/X:
* Text


<!-- 
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->
