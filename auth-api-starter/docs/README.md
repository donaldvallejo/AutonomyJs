# Autonomy

## Description
This API allows authenticated users to organise their time management.

## Intallation
To install Autonomy on your local machine, clone the repo, open your terminal, navigate to the directory you just created, and do the following:

```
npm install
```

from there, you can start the server by doing one of these:

```
npm start
```
Great, we are now ready for business.

# To DO's

## Get all To Do's

Send a GET Request on ```http://localhost:3000/todos``` and all To Do's will be returned in the order they were made.

## Get a specific To Do

Send a GET Request on  ```http://localhost:3000/todos/:enterIdHere``` to recieve the To Do whose ID you specified.

## Create a new To Do

Send a POST request on ```http://localhost:3000/todos``` and refer to following for names and values:

```js
name: String,
time: String,
description: String
```

The full HTTP request should look something like this:

`http://localhost:3000/todos?name=:name&gender=:gender&breed=:breed&age=:age`

Great.

## Update a To Do

Send a PUT request to ```http://localhost:3000/todos?_method=PUT``` and refer to following for names and values:

```js
name: String,
time: String,
description: String
```
Perfect.

## Delete a To Do

Send a DELETE request to ```http://localhost:3000/todos?_method=DELETE``` and refer to following for names and values:

```js
id: String
```

To Do go bye bye.

# Authentication

## Register an account

The first thing you'll have to do is solve the Google Captcha. This is in place so we can prevent spammers and bots.

All you'll have to do next is send a POST request to `http://localhost:3000/sign-up`  

Make sure you add the following headers with the correct data type:

```js
username: String,
password: Password
```

Then we will take care of the rest. This will also automatically log you in.

## Log in

In order to log in, send a POST request to ```http://localhost:3000/login```

Use the following headers with the correct data types:

```js
username: String,
password: Password
```

You should now be authenticated. You can check with the route below.

## Get current user

Send a GET request to:

`http://www.localhost:3000/current_user`

This will return the current req.user if you are authenticated, and will return undefined if you are not authenticated.

You can use this route to check rather or not you have authenticated succesfully.


## Log out

In order to log yourself out, you'll have to send a GET request to:

`http://localhost:3000/logout`

This will also clear your cookie. You can use the route above in order to check your login status. 
