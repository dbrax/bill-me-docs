---
id: home
blueprint: pages
title: Home
template: home
updated_by: b5e10532-9e62-4a0b-ade2-4803339d6a5b
updated_at: 1629570323
---
This is a documentation for   [Bill-me](https://github.com/dbrax/bill-me)  a thorough billing laravel package that is meant to help laravel developers 
who want to add billing features to their laravel application.

This package has the following features
- Order Management
- Invoice Management
- Receipt Management
- Order and Invoice Statistics
- Mail and Sms Notifications
- Order and Invoice Queries
- 
Once installed you can do stuff like this:

``` php

$billing=new BillMe;

//this will create an order and corresponding invoice
$billing->createOrder("emmanuel","Mnzava","epmnzava@gmail.com","","200","paypal","","Brooklyn Park",[["amount"=>"200","quantity"=>1,"Item"=>"Replacement Fee","description"=>"purchased moto moto"]],2);



```