# Remote-Access-of-Camera-Feed
In order to access your Raspberry Pi from anywhere, we need to be able to enter our home network! What is the only way of accessing it from anywhere? our IP address! It’s basically like a home address but on the internet.

However, most of home networks IP adresses change dynamically after a certain time. So let’s say we use it directly to access your PI, it would only work for a short time and then we’ll need to go home and check it again.

So we have to use a Fixed IP address which can be achieved by using DDNS Tool.
### Dynamic DNS with no-ip
To access my PI from anywhere, we use a service called Dynamic DNS or Domain Name Server. What does it involve?
- We choose a name for our home network that will redirect requests to an IP address stored on no-ip servers. Like http://mochi.ddns.net
- Should install the no-ip script in Raspberry PI. This will make sure that your home IP address stored on no-ip is always updated.
