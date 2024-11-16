# Ex02 Django ORM Web Application
## Date:12/11/2024 

## AIM
To develop a Django application to store and retrieve data from a bank loan database using Object Relational Mapping(ORM).

## ENTITY RELATIONSHIP DIAGRAM

![WhatsApp Image 2024-11-16 at 14 51 51_f9d87ed6](https://github.com/user-attachments/assets/b1586b95-f62b-4f82-a171-bf709f1ec7df)


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
  models.py

  
  from django.db import models
from django.contrib import admin
class Bank_loan (models.Model):
    customer_id=models.IntegerField(primary_key=True)
    customer_name=models.CharField(max_length=100)
    loan_amount=models.IntegerField()
    customer_age=models.IntegerField()
    email=models.EmailField()

class Bank_loanAdmin(admin.ModelAdmin):
    list_display=('customer_id','customer_name','loan_amount','customer_age','email')


    
admin.py


 from django.contrib import admin
from .models import Bank_loan,Bank_loanAdmin
admin.site.register(Bank_loan,Bank_loanAdmin)

## OUTPUT
![Screenshot (75)](https://github.com/user-attachments/assets/3e099207-ba71-4d3b-8bbe-f542e8893006)
![Screenshot (76)](https://github.com/user-attachments/assets/31f892c6-4a3d-4b9f-beb7-5eeba37b42fe)


## RESULT
Thus the program for creating a database using ORM hass been executed successfully
