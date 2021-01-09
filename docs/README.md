# System-design


### VPE's - Virtual private engine

- EC2
- GoDaddy

### Scaling 

- Vertical Scaling 

````
More resouces
Cost good money
more core, like two or quad core (literally can do 4 things at a time if Quad core).
Basically it does schedulling and more job cycles and it happens so fast that we dont realize even.
````

- Horizontal Scaling

````
Horizontal scaling is basically realizing that there is a upper limit and we dont want to hit that.

Load Balancer - so as to balance the traffic or distribute the traffic.

So now when user types in something.com you shall be directed to the Load Balancer ip address and let the load balancer decide on it to which server it will pass on the request to.

The Load balancer will now have public IP adresses. The server's can have private adresses now.

How Load Balancer will decide to whom it shall give the request to?

Load Balancer acts as DNS server
Can do Round robin method - Can't work in fairer way bcz still we will happen to send more load on one of the server than the another one.

TTl - Time to live

So a better approach shall be let the Load Balancer decides the same for who is bussiest.

session cookie keeps on expiring  and if somehow if the load balancer send you to a server diferent than the first time then you may have to login again and again.

Redundant array of Independent disk - RAID 0 , RADI 5 etc.

Use RAID to prevent the single point of failure, save cookies in mysql.
````

- Sticky sessions - even if you visit a website multiple times you gonna still end up on the same backend server.

- Shared Storage or Cookies 

Storage Cookies can be bad beacause it can have lot of personal thing. So storing at to which server the load balancer will pass it too , is a breach of security beacuse we dont want the world to know.

- Caching

.html
memcached - simply checks up for an ID which is currently not present in the cache, if its not it will fetch it from the SQL server. And if it then we have cached content and we need'nt go to the SQL which is an expensive operation to fetch the data.

garbage collector - remove the cached object based on the timestamp. So for example if an user has logged in and with the help of mem cached we have the oppurtunity to fetch the cache content then we can also update the timestamp for the user to the current time so as to have it still present in our cache memory.

- master master topology

- Partitioning

- High Availability

- Firewall - TCP.80,443

- Principal of the least previlage












