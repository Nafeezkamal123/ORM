# Ex02 Django ORM Web Application
## Date: 02-03-2024

## AIM
To develop a Django application to store and retrieve data from a Book database using Object Relational Mapping(ORM).

## Entity Relationship Diagram

![image](https://github.com/Abishai95141/ORM/assets/139335314/9777268b-d95b-4f2e-ba8e-e17389bad265)



## DESIGN STEPS

### STEP 1:
Clone the problem from GitHub

### STEP 2:
Create a new app in Django project

### STEP 3:
Enter the code for admin.py and models.py

### STEP 4:
Execute Django admin and create details for 10 books

## PROGRAM

```
models.py
from django.db import models
from django.contrib import admin 
class bookdb(models.Model):
    Bookid=models.IntegerField(primary_key=True)
    Bookname=models.CharField(max_length=20)
    Bookauthor=models.CharField(max_length=50)
    Bookprice=models.IntegerField()
    Bookgenre=models.CharField(max_length=20)
class BookAdmin(admin.ModelAdmin):
    list_display=("Bookid","Bookname","Bookauthor","Bookprice","Bookgenre")

admin.py
from django.contrib import admin
from .models import bookdb,BookAdmin
admin.site.register(bookdb,BookAdmin)
```

## OUTPUT

![image](https://github.com/Abishai95141/ORM/assets/139335314/01d89c7f-76f4-42f1-8ddb-b47df36aa904)



## RESULT
Thus the program for creating a database using ORM hass been executed successfully
