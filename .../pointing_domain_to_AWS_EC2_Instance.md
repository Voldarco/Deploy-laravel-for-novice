# Altschool Africa

## Mini-project

### In this exercise I use namecheap from my github-student pack to access a free domain name and Aws EC2 Instance. 

### This exercises is to document how to link your laravel project to a domain and connect using route 53 on Aws.

Much thanks to @Ceo_going_through_a_lot and @the_flower_pot_guy for making this possible with their assistance. 

## Getting started. 

#### for the free domain

First of all as an Altschool student you need to register
on github student pack under Altschool. Once you do this you'll be given a student developer pack. 

You can the go the this link <a href="https://education.github.com/experiences/virtual_event_kit">here</a> and check out the name cheap option.

**Note:** Only .me domains are free and you only get one so pick the name you want knowing you can't change it for at least a year. 

After you've secured the domain. You need to go to namecheap website and login in then visit your dashboard and checkout this tab. 


![IMG-20221028-WA0036_1667034470675](https://user-images.githubusercontent.com/69207791/198823669-93244738-8ef5-4691-874e-7aef401daa07.jpg)


#####  here are the steps: 

- Log in your name cheap account
- Go to the dashboard
- On the side, click domain list,
- Click mange
- Click advancedDNS
- Delete all A records
- Create a new A record using ‘@’ as the host then your AWS Public IP as value.
![Screenshot_20221028-212716_1667035515352](https://user-images.githubusercontent.com/69207791/198824209-86d3b355-4b41-43e4-a2cc-e943b560fdac.jpg)
- save. 

#### Linking Aws Instance.

- Open a new tab

- Log into your aws, then go to services and type route 53.

$screenshot.
- click on the first option.

- Click on create hosted zone. 
$screenshot. 

- Type in the domain name and click create hosted zone.
$screenshot.

- Click on create record.
$screenshot.

- Copy the the public IP address of your ec2 instance, paste inside the values field and create record. 
$screenshot. 






