# Entry 3
##### 02/29/24

Since my last blog entry, I completed my winter break goal with only 1-2 hours on learning and watching videos about Django, and get a good grasp of Django but I do not think I wouold be ready to tinker with Django yet. But I learned that Django has very nice powerful templating engine, that's purpose is separating HTML from python logic but that would require you to use django altogether, so it wouldn't be the best if we just wanted to set up a template for our website that we are going to make for the flashcards. 

I found a website that's called [Django Documentations](https://docs.djangoproject.com/en/5.0/topics/templates/), its basically like a example of an template but using djgango and python instead of mostly html. <br>
#### Syntax<br>
The syntax of the Django template language involves four constructs.
* Variables
* Tags
* Filters
* Comments

#### Variables<br>
Variables are surrounded by {{ and }} like this:
```
My first name is {{ first_name }}. My last name is {{ last_name }}.
```
With a context of {'first_name': 'John', 'last_name': 'Doe'}, this template renders to:
```
My first name is John. My last name is Doe.
```
The variables is basically the same thing as you would do in JS or Java, it will fill in as what you stored in the variable. 

#### Tags<br>
Tags provide arbitrary logic in the rendering process. For example, a tag can output content, serve as a control structure e.g. an “if” statement or a “for” loop, grab content from a database, or even enable access to other template tags.<br>
Tags are surrounded by {% and %} like this:
```
{% csrf_token %}
```
Most tags accept arguments:
```
{% cycle 'odd' 'even' %}
```
Some tags require beginning and ending tags:
```
{% if user.is_authenticated %}Hello, {{ user.username }}.{% endif %}
```
This is also known as an built in tags because as you can see it's mixed in with the variable. 

#### Filters <br>
Filters transform the values of variables and tag arguments. They look like:
```
{{ django|title }}
```
With a context of {'django': 'the web framework for perfectionists with deadlines'}, this template renders to:
```
The Web Framework For Perfectionists With Deadlines
```
Some filters take an argument:
```
{{ my_date|date:"Y-m-d" }}
```

#### Comments <br>
A {# comment #} tag provides multi-line comments.
Comments look like this:
```
{# this won't be rendered #}
```

#### Components <br>
* Engine
* Template
* Context

#### Engine 

Django.template.Engine encapsulates an instance of the Django template system. The main reason for instantiating an Engine directly is to use the Django template language outside of a Django project.
When instantiating an Engine all arguments must be passed as keyword arguments:

* dirs is a list of directories where the engine should look for template source files. It is used to configure filesystem.Loader.

It defaults to an empty list.

* app_dirs only affects the default value of loaders. See below.

It defaults to False.

* autoescape controls whether HTML autoescaping is enabled.

It defaults to True.

#### Template 

The recommended way to create a Template is by calling the factory methods of the Engine: get_template(), select_template() and from_string().

In a Django project where the TEMPLATES setting defines a DjangoTemplates engine, it’s possible to instantiate a Template directly. If more than one DjangoTemplates engine is defined, the first one will be used.

class Template¶
This class lives at django.template.Template. The constructor takes one argument — the raw template code:
```
from django.template import Template

template = Template("My name is {{ my_name }}.")
```

#### Context 
Once you have a compiled Template object, you can render a context with it. You can reuse the same template to render it several times with different contexts.

class Context(dict_=None)

The constructor of django.template.Context takes an optional argument — a dictionary mapping variable names to variable values.

For details, see Playing with Context objects below.

Template.render(context)
Call the Template object’s render() method with a Context to “fill” the template:
```
>>> from django.template import Context, Template
>>> template = Template("My name is {{ my_name }}.")

>>> context = Context({"my_name": "Adrian"})
>>> template.render(context)
"My name is Adrian."

>>> context = Context({"my_name": "Dolores"})
>>> template.render(context)
"My name is Dolores."
```
 
At the end we still are trying to figure out what we want to do with our website. But we do have an idea of what the MVP is looking like and which parts me and my partner would need to work on to achieve what we want the webiste to function. The skills I used during this time period was "growth mindset" and "embracing failure" because I have little to no clue what was going on when I was watching those video, I only knew the code worked. But I also taken to consideration that when we create the website, how I want it to look and how we going to make it. So eventually we would need a template. Overall, this only would get me thinking of what I really need to know before I start coding my website. 


[Previous](entry02.md) | [Next](entry04.md)

[Home](../README.md)
