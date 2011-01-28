!SLIDE
# REST #
## Representational State Transfer ##

!SLIDE smbullets small
# Huh? #
* REST is an archetectural style for client server interactions
* It's based on the concept of limited verbs (methods) but unlimited nouns (identifiers)
* The only methods generally used in REST are GET, POST, PUT, and DELETE
* Resources are identified by their.. wait for it.. identifiers.  URIs

!SLIDE smbullets small
# Verb That Noun! #
* You probably know these.  Your web browser does them all the time.
* POST - Create something new.  Ex:  A form posting your credit card data creates a new transaction
* GET - Return a resource.  Ex:  A get call on a URI returns a web page

!SLIDE smbullets small
# Verb That Noun Again! #
* These not so much.  Websites don't really use this part of HTTP.
* PUT - Update a resource.  Ex:  Change information on a previous transaction.
* DELETE - Delete a resource.  Ex:  Cancel a transaction.

!SLIDE smbullets small
# Why Is REST Different Than SOAP? #
* REST doesn't really have contracts.  Everyone knows what the methods are on any location.
* REST is pretty lightweight.  It's not all wrapped up in XML.
* SOAP has a more rigid structure.  The consumer of a SOAP service knows what to expect.
* REST calls are really cheap.  Calling applications probably understand an HTTP request but may need a framework to easily consume SOAP.

!SLIDE smbullets small
# When To Use REST #
* REST is great when you are communicating between your own client and server
* It's also pretty good when dealing with high frequency low importance type applications (think Twitter) since it saves on bandwidth and the lack of a contract is pretty tolerable

!SLIDE smbullets small
# When Not To Use REST #
* Don't use REST when you want to publish enterprise services to someone else
* Don't use REST when you want to configure all your own methods

!SLIDE smbullets small
# Additional Notes #
* WCF can do REST instead of SOAP (example [here](http://consultingblogs.emc.com/anthonysteele/archive/2008/03/15/rest-from-wcf-3-5.aspx))
* REST works very nicely with JSON.  Your RESTful service can communicate quite easily with something like a jQuery .ajax call

!SLIDE
# Questions? #
