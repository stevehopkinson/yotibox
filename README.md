# YotiBox
Platform for creating virtual addresses using Yoti, for use by people who have no traditional address or identification.

## Wireframes
![Customer front-end](https://github.com/stevehopkinson/yotibox/blob/master/wireframes/YotiBox%20-%20Front%20End.png?raw=true)


![Admin front-end](https://github.com/stevehopkinson/yotibox/blob/master/wireframes/YotiBox%20-%20Admin%20Front%20End.png?raw=true)


![Collection interface](https://github.com/stevehopkinson/yotibox/blob/master/wireframes/YotiBox%20-%20Collection%20Point.png?raw=true)



## Database Schema
![Database Schema](https://github.com/stevehopkinson/yotibox/blob/master/wireframes/YotiBox%20%E2%80%93%20Database%20Schema.png?raw=true)


## Routes
* ```GET /```: Default route. Shows 'Connect with Yoti' if user isn't authenticated. Shows dashboard if user is authenticated.
* ```GET /admin```: Admin route. Shows login interface and prompts admin to select location if not authenticated. Shows interface to register a parcel if admin is authenticated.
* ```POST /register_delivery```: Allows administrator to register a delivery to a YotiBox.
* ```GET /collection_point```: Allows admin to log in to set up a terminal as a collection point. If logged in, shows the relevant Yoti code for the user to scan for that collection point.
* ```GET /show_deliveries```: Shows all deliveries currently ready for collection for that user at that location.
* ```POST /mark_collected```: Allows collection point to mark that a parcel has been collected.
