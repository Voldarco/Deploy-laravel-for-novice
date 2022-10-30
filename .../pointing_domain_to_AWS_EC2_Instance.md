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
- Click manage
- Click advancedDNS
- Delete all A records
- Create a new A record using ‘@’ as the host then your AWS Public IP as value.
![Screenshot_20221028-212716_1667035515352](https://user-images.githubusercontent.com/69207791/198824209-86d3b355-4b41-43e4-a2cc-e943b560fdac.jpg)
- save. 

#### Connecting Aws Instance.

- Open a new tab

- Log into your aws, then go to services and type route 53.

![Screenshot_20221028-211858_1667036233145](https://user-images.githubusercontent.com/69207791/198827741-e9ce294f-0da5-4a58-8597-aa5518fb4d01.jpg)

- click on the first option.

- Click on create hosted zone.
 
![Screenshot_20221028-214701_1667036528641](https://user-images.githubusercontent.com/69207791/198827790-e33685ef-164c-42db-82d1-bfc6be87b060.jpg)


- Type in the domain name and click create hosted zone.

![Screenshot_20221028-215024_1667036827876](https://user-images.githubusercontent.com/69207791/198827843-eb45feab-a058-4ab5-96ff-995f70abf19a.jpg)

- Click on create record.

![Screenshot_20221028-215359_1667037030928](https://user-images.githubusercontent.com/69207791/198827894-51ccbdaa-856b-41af-9c7e-3b0bf4c9d5e7.jpg)


- Copy the the public IP address of your ec2 instance, paste inside the values field and create record. 

![Screenshot_20221028-215931_1667037377746](https://user-images.githubusercontent.com/69207791/198827933-0bcf200a-9f18-4221-a619-dfd499331796.jpg)


Click on create record again.

- In the first typing field, i.e the one above the first drop-down menu, type **www**
- For the drop-down menu change it to **C-Name**
- In the values field, i.e first typing field after drop-down menu, type your domain name.

![Screenshot_20221028-220834_1667037617928](https://user-images.githubusercontent.com/69207791/198827969-66b16b8f-7494-448f-b896-dbed18f540b3.jpg)

- Click on create. 

#### Linking your AWS instance to your domain. 

Congrats on getting this far.
Now head over to your namecheap domain or the domain you used above.

- Go to the dashboard
- On the side, click domain list,
- Click mange
- Scroll down and Search for a section on DNS or nameservers.

![Screenshot_20221028-221827_1667038491025](https://user-images.githubusercontent.com/69207791/198828075-7189aabc-e6a4-4593-8572-77daba0d39ab.jpg)


- Now change that option from **NameCheap BasicDNS** to **Custom DNS** 

![Screenshot_20221028-222257_1667041871016](https://user-images.githubusercontent.com/69207791/198828173-5ef6445b-02a1-427e-bc44-33121a9bb508.jpg)


- Copy the 4 DNS values from the hosted zone on your AWS route 53 area and paste them in each field for the Custom DNS. 

![IMG-20221028-WA0068_1667041993762](https://user-images.githubusercontent.com/69207791/198828272-2999108d-428d-40fd-8c1a-4fd713023d66.jpg)


- Once you've done this for all 4 DNS. Save your settings on NameCheap. And that's all. The settings would reflect anywhere from between 30 mins - 48 hours. Once it's reflected, your url should now be able to lead you to your Laravel default page

![Screenshot_20221028-223619_1667042211339](https://user-images.githubusercontent.com/69207791/198828393-236bed20-061f-484a-821f-f71796ee1454.jpg)


This has been a great journey and you can always come back to this in the future for review. 





