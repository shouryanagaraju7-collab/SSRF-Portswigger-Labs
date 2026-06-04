Title:Basic SSRF against another back-end system

Objective: use the stock check functionality to scan the internal 192.168.0.X range for an admin interface on port 8080, then use it to delete the user carlos. 

we will first send the stock request to the repeater.

![alt text](image.png)

then we will change the stock API as follows:

![alt text](image-1.png)

we still don't know which system does the admin reside so we will send this request to the intruder and check for each device .

![alt text](image-2.png)

then we will add the $$ on 192.168.0.$1$ and then initiate the sniper attack :

![alt text](image-3.png)

we will change the payload settings as follows:
![alt text](image-4.png)

the we start the attack and when we get the 200ok message it means that we found the right device.

![alt text](image-5.png)

with this we go the ip of admin as 192.168.0.156 so now we delete carlos by changing the url as follows:

![ alt text](image-6.png)

and then send to complete the lab.


