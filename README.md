# Ex02 Django ORM Web Application
## Date: 05.10.2025

## AIM
To develop a Django application to store and retrieve data from a Car Inventory Database using Object Relational Mapping(ORM).

## ENTITY RELATIONSHIP DIAGRAM



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
model.py
from django.db import models
from django.contrib import admin
class Car(models.Model):
    car_name = models.CharField(max_length=255, help_text="Car Name")
    car_model = models.CharField(max_length=100, help_text="Car Model")
    registration_number = models.CharField(max_length=50, unique=True, help_text="Registration Number")
    color = models.CharField(max_length=50, help_text="Car Color")
    insurance = models.CharField(max_length=100, help_text="Insurance Details")
    price = models.DecimalField(max_digits=10, decimal_places=2, help_text="Current Price in INR")

class CarAdmin(admin.ModelAdmin):
    list_display = ('car_name', 'car_model', 'registration_number', 'color', 'insurance', 'price')

admin.py
from django.contrib import admin
from .models import Car,CarAdmin
admin.site.register(Car,CarAdmin)
```

# Register your models here.


## OUTPUT

![alt text](<Screenshot 2025-10-05 121307.png>)

## RESULT
Thus the program for creating car inventory database database using ORM hass been executed successfully
