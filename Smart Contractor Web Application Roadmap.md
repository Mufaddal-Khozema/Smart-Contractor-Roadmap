___
# Product Requirements
- [[#Step 1 Login via Facebook/Google|Login via Facebook/Google]]
- User can add Display Picture & Phone number.
- User can add services.
- [[#Step 2 User sees thier contacts|User can view from contacts, who is registered on this application, and can view profiles.]]
- User’s locations should be taken. 
- Show the list of skillful users nearest (under 10km) to him
- User can search the required service by categories, location or contacts.
- User can send offer to a person any rate, another user can accept/reject the offer. They can chat with each other.
- Upon hiring, both users will see their live locations on map, the best routes from source to destiny.
- User canwrite a review for a service and can rate by using five star ratings & end the contract
- Admin can login via specific credentials.
- Admin can view/block/delete the users.
- Admin can add categories.
- Admin can chat/warn to any user.
- Admin can see/filter the weekly, monthly & yearly hirings graphs on dashboard.
___
# Functionality Already Implemented
- Login via email/password
- User can add Display Picture & Phone number.
- User can add services.
___
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
    "profile_photo": "/uploads/namelast.png"
}
```
## Step 1: Login via Facebook/Google
1. Use the Facebook and Google PHP SDK to allow user to signup/login with thier Google/Facebook account
2. Retireve details about the user from the platform they are trying to sign up with
3. Resurface the form but now filled with some details for their social sign in accounts
4. Make the user.
## Step 2: User sees thier contacts 
1. Gain access to users contact information
2. Notify the user about contact that use the service. Give them an option to add them as friends.
##

