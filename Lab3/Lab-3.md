Title:SSRF with blacklist-based input filter

Objective: , change the stock check URL to access the admin interface at http://localhost/admin and delete the user carlos.

we will first send the stock request to the repeater.

![alt text](image.png)

when we use localhost we get an resriction :
![alt text](image-1.png)

we will ise 127.1 in teh place of local host:

![alt text](image-2.png)

we still got 400 bad request lets url encode the a in admin(%61)  to see if we can get the access:

![alt text](image-3.png)

we still got a 400 bad request so we double url encode a (%25%36%31):

![alt text](image-5.png)

now we got a 200 ok message and can see the admin panel to delete the user carls just add /delete?username=carlos to the stockapi

![alt text](image-6.png)

with this you have solved the lab.



