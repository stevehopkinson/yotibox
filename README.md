# YotiBox
Platform for creating virtual addresses using Yoti, for use by people who have no traditional address or identification.

## In brief
YotiBox gives people without fixed addresses a unique virtual address linked to their Yoti ID, allowing them to receive key mail deliveries that help them get back on their feet.

## Problem that YotiBox solves.
Many of the services that we take for granted require a fixed address for registration or delivery – job applications, registering with a GP, applying for a bank account, and so on. If people do not have access to a fixed address, they often end up in a vicious circle of not being able to get back on to their feet bceause the things that they require all depend on having an address.

There is no good solution to this problem. Collecting postage from a business usually requires people to present photo ID in the form of a driving licence or passport – something that many people without fixed addresses don't have access to. The alternative is to rely on informal arrangements – having post delivered to a church, or a friendly neighbour, or a business. But these solutions lack security and depend on such institutions agreeing to help.

YotiBox would provide people with the facility to register a 'YotiBox' – a virtual address linked to their Yoti ID. Users can then use that address for deliveries, receive notifications when a delivery is made to their YotiBox, and use Yoti to confirm their ID and collect parcels from the collection point.

Each virtual 'address' is uniquely linked to the user's Yoti ID, so staff at the collection point simple need to register that a delivery has been made to the specified address, and the user will instantly be notified.

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
