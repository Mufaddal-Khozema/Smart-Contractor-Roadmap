# Product Requirements
- [Login via Facebook/Google](#step-1-login-via-facebookgoogle)
- User can add Display Picture & Phone number.
- User can add services.
- [User can view from contacts, who is registered on this application, and can view profiles.](#step-2-user-sees-thier-contacts)
- [User’s locations should be taken. ](#step-3-users-locations-should-be-taken)
- [Show the list of skillful users nearest (under 10km) to him](#step-4-show-the-list-of-skillful-users-nearest-under-10km-to-him)
- [User can search the required service by categories, location or contacts.](#step-5-user-can-search-the-required-service-by-categories-location-or-contacts)
- [User can send offer to a person any rate, another user can accept/reject the offer. They can chat with each other.](#step-6-user-can-send-offer-to-a-person-any-rate-another-user-can-acceptreject-the-offer-they-can-chat-with-each-other)
- [Upon hiring, both users will see their live locations on map, the best routes from source to destiny.](#step-7-upon-hiring-both-users-will-see-their-live-locations-on-map-the-best-routes-from-source-to-destiny)
- [User canwrite a review for a service and can rate by using five star ratings & end the contract](#step-8-user-canwrite-a-review-for-a-service-and-can-rate-by-using-five-star-ratings-end-the-contract)
- Admin can login via specific credentials.
- Admin can view/block/delete the users.
- Admin can add categories.
- Admin can chat/warn to any user.
- Admin can see/filter the weekly, monthly & yearly hirings graphs on dashboard.
# Functionality Already Implemented
- Login via email/password
- User can add Display Picture & Phone number.
- User can add services.
# Functionality `To` Implement **(In Stepwise Order)**
##  Step 0:
Currently the user table has only id, email and password. To accomodate the rich user personal details required for this project the schema has to be altered as so.  
```
// Users Table
{
    "first_name": "name",
    "last_name": "last",
    "email":"namelast@gmail.com",
    "mobile": 1234567890,
    "street_address": "Abc Steet, Loop Rd, Pqr Town",
    "city": "Lahore",
    "province": "Punjab",
    "zip_code": 05499,
    "trade": "Canpenter",
    "skill": "Apprentice 1",
    "looking_to_worki_in": "Karachi",
    "password":"&^&^@*@($JBSJJBV@sjwb3*",
    "profile_photo": "/uploads/namelast.png",
    "location": "",
}
```
## Step 1: Login via Facebook/Google
1. Use the Facebook and Google OAuth PHP to allow user to signup/login with thier Google/Facebook account
2. Retireve details about the user from the platform they are trying to sign up with
3. Resurface the form but now filled with some details for their social sign in accounts
4. Make the user.
## Step 2: User sees thier contacts 
1. Gain access to users contact information
2. Notify the user about contact that use the service. Give them an option to add them as friends.
## Step 3: User’s locations should be taken. 
1. Prompt the user to provide the website with thier location.
2. The location should be saved in the database under the Users table.
3. Use the location to query location [features.](#step-4-show-the-list-of-skillful-users-nearest-under-10km-to-him)
## Step 4: Show the list of skillful users nearest (under 10km) to him
1. If the user doesn't have location enable ask agian for thier permission for location accesss.
2. Query the databse to filter the service providers nearest to the user.
## Step 5: User can search the required service by categories, location or contacts.
1. Search will have an addition button for filtering search results.
2. Searching [location](#step-4-show-the-list-of-skillful-users-nearest-under-10km-to-him) will depend on the location enable. The search results will be ordered in proximity to the user
3. Categories here is understood as the types of trade a service provider provides. The search result with those trades will be shown at the top.
4. Contact here is understood as both the contacts on thier mobile phone and the friends they have added/service provider that they are have had any interaction with. The service providers fitting the aforementioned criterion will be shown in the search result first.
## Step 6: User can send offer to a person any rate, another user can accept/reject the offer. They can chat with each other.
1. This feactures rests in the center of many of the core feature of the application. I will discuss those feature here with varying levels of details.
2. Service providers: They are users that have opt in to be service providers. They can have a description and display thier various services. They will also be accompanied by [rating].
3. User chatting: User has the option to contact a service provider if they so choose. To enable this chatting there will be a chats view where a person will see all the users that they have engaged in chats with. 
4. Offer sending: An offer is proposition that a user can approach in two ways. A Service provider will have an option on thier profile 'send an offer'. The second way is in chatting where the same option will be available and can be utilised by the user anytime. The offer will look something like, where an they will be given an offer page where the user will provide a **'title'** (to describe what they want), **'service/s'** (This will be the type of service or services the user needs from the service provider), **'explanation'** (Here the user can go more into detail in what they need from the services provider), **'expected timeline'** (The user can provide the time they expect the project) and **'price'** (The price at which they wish to comission the project).
5. Offer response: A Service provider after recieving an offer has the option to accept/renegotiate/reject the offer all will be (optionally) accomanied by a message by the Service provider. Only the accept option will trigger a job.
6. Scheduling a job: After the job has been decided. The user can go to the my jobs page to schedule a job or request the job right now. [job](#step-7-upon-hiring-both-users-will-see-their-live-locations-on-map-the-best-routes-from-source-to-destiny).
## Step 7: Upon hiring, both users will see their live locations on map, the best routes from source to destiny.
1. Jobs page: a user and Service Provider will have a my jobs page that will include all the jobs they are currently engaged in and all all thier past jobs.
2. Job event: when a job is triggered there will be a waiting menu for the Service Provider to opt in and an option to send a message.  After the service provider opts in, both will see each others adress and the best routes for each other to meet.
## Step 8: User canwrite a review for a service and can rate by using five star ratings & end the contract.
1. After a job event is successfully over and the user will have a option on the [job page](#step-7-upon-hiring-both-users-will-see-their-live-locations-on-map-the-best-routes-from-source-to-destiny) to write them a review.