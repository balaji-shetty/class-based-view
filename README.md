ChatGPT Prompt - https://grok.com/share/c2hhcmQtMg%3D%3D_72249f13-5d41-4111-aa86-aa76727d2105

Django Blog Project – Command Index (For Teachers & Students)
Here is a complete step-by-step command list you followed to build the CRUD Blog Dashboard with tabular display.

1. Setup Project
bash


mkdir myblog
cd myblog
--------------------------------------------------
python -m venv venv
# Windows
venv\Scripts\activate

# Mac/Linux
source venv/bin/activate
**************************
pip install django
django-admin startproject myblog .
python manage.py startapp blog
Register app in myblog\setting.py
*******************************

Create \templates folder under app \blog

mkdir blog/templates
python manage.py makemigrations
python manage.py migrate
python manage.py createsuperuser

python manage.py runserver
********************************

URL  in Browser

 http://127.0.0.1:8000/

It display all articles and link 
1> Add new article by showing the form
     Enter Title - 
     Write content -
             / ADD Article Button /
2> Display all records in Articles models
3> Button to Edit (http://127.0.0.1:8000/article/1/edit/)
3> Button to Delete (http://127.0.0.1:8000/article/5/delete/)

Edit -    http://127.0.0.1:8000/article/1/edit/

Delete - http://127.0.0.1:8000/article/5/delete/

4. Key Files Created
   
File,Purpose
blog/models.py,"Define Article (title, content, dates)"

blog/admin.py,Show articles in /admin

blog/views.py,"dashboard, article_detail, edit, delete"

blog/urls.py,"All URLs (/, /article/1/, /edit/, /delete/)"


myblog/urls.py,Include blog.urls
blog/templates/dashboard.html,Table view + Add form

blog/templates/article_detail.html,View full article

blog/templates/article_form.html,Edit form

blog/templates/article_confirm_delete.html,Delete confirm

5. Final URLs (Students Can Test)
   URL,Action
http://127.0.0.1:8000/,Dashboard – Add + Table

http://127.0.0.1:8000/article/1/,View article

http://127.0.0.1:8000/article/1/edit/,Edit

http://127.0.0.1:8000/article/1/delete/,Delete

http://127.0.0.1:8000/admin/,Admin panel
