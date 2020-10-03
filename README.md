# Remote-Access-of-Camera-Feed-Through-Internet
In order to access your Raspberry Pi from anywhere, we need to be able to enter our home network! What is the only way of accessing it from anywhere? our IP address! It’s basically like a home address but on the internet.
![](https://github.com/anoopcc99/Remote-Access-of-Camera-Feed/blob/master/images/RemoteAccess1.png)

However, most of home networks public and private IP adresses change dynamically after a certain time. So let’s say we use it directly to access your PI, it would only work for a short time and then we’ll need to go home and check it again.
![](https://domoticproject.com/wp-content/uploads/2017/12/InternalVsExternalIP.png)
So to have Fixed internal IP address for Raspberry Pi we need to assign static IP address through DHCP Server.

So we have to use a Fixed IP address which can be achieved by using DDNS Tool.
### Dynamic DNS with no-ip
To access our PI from anywhere, we use a service called Dynamic DNS or Domain Name Server. What does it involve?
- We choose a name for our home network that will redirect requests to an IP address stored on no-ip servers. Like http://mochi.ddns.net
- We Should install the no-ip script in Raspberry PI. This will make sure that your home IP address stored on no-ip is always updated.

![](https://hackernoon.com/hn-images/1*HLZbT1WKXNzK_cda9AP2kQ.png)

### Configure the port forwarding to your PI
 We have a domain name that always redirects to our home network. However, our internet box (a.k.a router) doesn’t know how to deal with the incoming requests! We need to ask “Hey please, redirect incoming requests to the Raspberry Pi”. All routers are different, the best thing to do is to search “Port forwarding” on the web with available brand and model. The main things we have to do, This the TCP layer which deals with process-process delivery.
 ![](https://hackernoon.com/hn-images/1*1TZhxFzf_U6OEKceMSR1CA.png)
- Internal Port: The port on the raspberry Pi where requests should be redirected to. In our case, the video stream server is at 8081.

- External Port: We don’t want ALL requests redirect to our PI. Only those that are targeting the camera server. Since we are going to use a browser, or an app to access our Pi, we can request our home network with any port we want. (for example we will use http://mochi.ddns.net:XXXX). To make it simple, we used the same as the video stream server: 8081.
