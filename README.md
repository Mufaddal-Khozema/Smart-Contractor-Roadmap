# Product Requirements
- [Login via Facebook/Google](#step-1-login-via-facebookgoogle)
- User can add Display Picture & Phone number.
- User can add services.
- [User can view from contacts, who is registered on this application, and can view profiles.](#step-2-user-sees-thier-contacts)
- [User’s locations should be taken. ](#step-3-users-locations-should-be-taken)
- [Show the list of skillful users nearest (under 10km) to him](#step-4-show-the-list-of-skillful-users-nearest-under-10km-to-him)
- User can search the required service by categories, location or contacts.
- User can send offer to a person any rate, another user can accept/reject the offer. They can chat with each other.
- Upon hiring, both users will see their live locations on map, the best routes from source to destiny.
- User canwrite a review for a service and can rate by using five star ratings & end the contract
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
1. Use the Facebook and Google PHP SDK to allow user to signup/login with thier Google/Facebook account
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

