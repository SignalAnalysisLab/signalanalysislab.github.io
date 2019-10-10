sal.guide is a simplistic webpage created for fast navigation of SAL services.
The code is intentionally very minimal, and based on the simple getskeleton.com boilerplate, in order to get a nice looking webpage both on desktop and mobile up and running fast.

The sal.guide domain is managed by proisp.
sal.guide points to the Trondheim SAL network.
The end router routes all HTTP and HTTPS requests to our apache gateway server VM on HAL.
The apache gateway server serves sal.guide directly in a VirtualHost directive, serving the folder /var/www/html/ from its local storage.

Some might argue that displaying services like these out in the open is a bad security practice. 
However, we disagree in the fact that "hiding" what services we use is security by obscurity - which easily fails when used services are known anyway. 
In other words, we believe that the security should lie in the services themselves. If an attacker only needs to know what service we use in order to successfully breach us, the security must be fundamentally flawed to begin with. An unsecure service should never be exposed on a public network.

Also, remember the security triangle: CIA. Confidentiality, Integrity, and Availability. We want our services to be confidential, that its data integrity is secured, but just as important is that it needs to be available to employees when needed.
sal.guide ensures that all services are easily available to any employee. Putting a password in front of it quickly makes it more tedious than just typing in that awful long url to begin with.
