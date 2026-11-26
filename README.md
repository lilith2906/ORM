# Ex02 Django ORM Web Application
## Date:19/11/2026 

## AIM
To develop a Django Application to store and retrieve data from a E-Commerce Website Database for Amazon or Flipkart using Object Relational Mapping(ORM).


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
from django.contrib import admin
from .models import Car,CarAdmin

admin.site.register(Car, CarAdmin)

from django.db import models
from django.contrib import admin


class Car(models.Model):

    car_id = models.CharField(
        max_length=20,
        primary_key=True,
        help_text="Car ID"
    )

    brand = models.CharField(max_length=100)

    model = models.CharField(max_length=100)

    year = models.IntegerField()

    price = models.IntegerField()

    fuel_type = models.CharField(max_length=50)

    quantity = models.IntegerField()

    color = models.CharField(max_length=50)

    def _str_(self):
        return self.brand + " " + self.model


class CarAdmin(admin.ModelAdmin):

    list_display = (
        'car_id',
        'brand',
        'model',
        'year',
        'price',
        'fuel_type',
        'quantity',
        'color'
    )
```



## OUTPUT

![alt text](<Screenshot 2026-11-26 113313.png>)


## RESULT
Thus the program for creating E-commerce website database using ORM hass been executed successfully
