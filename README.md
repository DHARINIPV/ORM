# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram

![image](https://user-images.githubusercontent.com/119400845/211877446-d2f208fa-2942-496f-875f-f3fe24a4a959.png)


## DESIGN STEPS

### STEP 1:
Clone the problem from github.
### STEP 2:
create new app.
### STEP 3:
Enter the code of admin.py and model.py.
### STEP 4:
Execute Django admin and create 10 employees.

## PROGRAM

```
Model.py
from django.db import models
from django.contrib import admin
# Create your models here.
class Employee(models.Model):
    Emp_id=models.CharField(primary_key=True,max_length=150,help_text='Emplopee_id')
    name=models.CharField(max_length=100)
    salary=models.IntegerField()
    age=models.IntegerField()
    email=models.EmailField()

class EmployeeAdmin(admin.ModelAdmin):
    list_display=('Emp_id','name','salary','age','email')
    
Admin.py
from django.contrib import admin
from .models import Employee,EmployeeAdmin

admin.site.register(Employee,EmployeeAdmin)
```

## OUTPUT
![image](https://user-images.githubusercontent.com/119400845/211870247-41b87bd6-9934-4dc1-90cb-d1124b4b987c.png)

## RESULT
program excuted successfully.
