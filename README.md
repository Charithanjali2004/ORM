# Ex02 Django ORM Web Application
# Date:30-09-2024
# AIM
To develop a Django application to store and retrieve data from a bank loan database using Object Relational Mapping(ORM).

# ENTITY RELATIONSHIP DIAGRAM
## DESIGN STEPS
## STEP 1:
Clone the problem from GitHub

## STEP 2:
Create a new app in Django project

## STEP 3:
Enter the code for admin.py and models.py

## STEP 4:
Execute Django admin and create details for 10 books

# PROGRAM
```# model.py
from django.db import models

# Create your models here.
from django.db import models
from django.contrib import admin

class Loan(models.Model):
    loan_id = models.AutoField(primary_key=True)
    customer_name = models.CharField(max_length=100)
    loan_amount = models.DecimalField(max_digits=10, decimal_places=2)
    interest_rate = models.DecimalField(max_digits=5, decimal_places=2)
    loan_term = models.IntegerField()
    disbursement_date = models.DateField()

class LoanAdmin(admin.ModelAdmin):
    list_display=('loan_id','customer_name','loan_amount','interest_rate','loan_term','disbursement_date')
```

```# admin.py
from django.contrib import admin

# Register your models here.
from .models import Loan,LoanAdmin

admin.site.register(Loan,LoanAdmin)
```
# OUTPUT
Include the screenshot of your admin page.
![Screenshot (71)](https://github.com/user-attachments/assets/5d6244db-90a7-4a88-8237-d13aabbc2ea3)
![Screenshot (67)](https://github.com/user-attachments/assets/bf3fad45-356f-44c3-b9ef-3d0960e9e81f)
![Screenshot (68)](https://github.com/user-attachments/assets/2ea91fef-47e2-43c1-b17d-ba597433e58b)
![SERVER EX-5](https://github.com/user-attachments/assets/de4b4da0-c62d-486a-8175-22f4fcfaab4c)









# RESULT
Thus the program for creating a database using ORM hass been executed successfully
