This is the readme from the project repository that is stored on the private university Git Enterprise server.

# Looking 4 Gamers

The app 'Looking 4 Gamers' was created with the intention to provide an easy way for gamers to connect and play with eachother in various online games. Through the app, a large array of pages corresponding to real video games is accessible to the user, with each page functioning as a user hub for coordination of multiplayer gaming online. The games available in the app are fetched from a third party API which hosts a large database storing video game information. The user has access to a login, profile page and the various user parties that are set up in the app. One can either join an existing party linked to a specific game, or create a new party and become its host. Each user can be active in one party at a time. The app is created using MVP architecture, where the functionalities are split up into model, viewer and presenter. 

## Technologies used

* [RAWG Video Games Database API](https://rawg.io/apidocs)
* [Firebase](https://firebase.google.com/)
* [Javascript](https://www.javascript.com/)
* [HTML](https://html.spec.whatwg.org/)
* [CSS](https://www.w3.org/TR/CSS/#css)
* [Vue](https://vuejs.org/)
* [JSX](https://reactjs.org/docs/introducing-jsx.html)
* [Babel](https://babeljs.io/)

## Getting Started

The app is reached by inserting the URL 'https://looking4gamers-ff8a3.web.app/' into a web browser, from a device free of choice. The user is then greeted by a 'landing page' containing guidance and basic information about the site when first opening up the app. From there, one can either signup a new account or choose to log in from an already existing one. Signing up requires two inputs taking email address and password. A first time user is given a randomized screen name which can be changed from the profile page, which is available once the user has signed in.

## Functions

### Sign up

Sets up a new user and creates an account. Takes email and password as user inputs.

### Log in

Allows an existing user to log in, under the condition that the user account already exists and the email and password inputs matches said account.

### Log out 

Logs out the user from the app. The functionality of the app is closed until logged in again.

### Profile editor

Edits the user profile. The user is able to change its profile settings. Screen name, Steam ID, PSN username, Xbox gamertag, Switch friendcode are taken as string inputs. Preferred game platforms can be set for more personalized user experience.

### Search

Searches through the game database fetched from RAWG. Returns a list of games matching the search input. 

### Details

Renders game information from a chosen game. Makes use of both RAWG and the user information from Firebase.

### Create party

Creates a new party linked to a specific game, with its parameters and conditions being set by the user who becomes the party's host. Can only be done if the user isn't alrady in a party.

### Join party

Enables the user to join an existing party. Can only be done if the user isn't alrady in a party.

### Leave party

Enables the user to leave a party that he/she no longer wishes to be a part of.

### Delete party

Enables the host of the party to delete said party, and all of the party members leave the party as result. 

## Database structure

### Users:
* user_id
* display_name
* steam_id
* psn_id
* xbox_id
* preferred_platforms
* hosting_party BOOLEAN
* in_party BOOLEAN

### Party:
* game
* title
* description
* party_size
* party_members
* how_to_join
* platform

## Usage

The app is aimed for everyone who enjoys playing video games in general, and multiplayer games in particular. With its minimalistic and simplified design, the app is accessible to anyone looking to play online games, no matter technical competence and experience level. A smooth and clear user experience was prioritized for that very reason.

We imagine that average user experience could go as follows: 

A user with the intention to play a multiplayer game online and who's looking for other players to play with logs onto the app. The user then finds the game that he/she intends to play through the use of the search bar in the header. Once on the page for the intended game, the user is then able to either join up with a party or create a new one. Perhaps he/she finds a party filled with friends in the list containing all the game parties, and therefore decides to join up with that party for a gaming session. Or he/she might prefer to become a host and set the parameters to his/her own liking. From there the party members can easily find each other's information and communication channels. It's all up to the user, the app is only here to provide a platform enabling human connections among people with similar interests.

## Deployment

As a way of getting the app online and accessible to users outside of the immediate project group, we deployed the app to the internet using Firebase's hosting solution. 

## Contact

Fredrik Svanholm - svanhol@kth.se
Lucas von Schéele - lucasvs@kth.se
Durim Sadiku - durim@kth.se
Jimmy Mäkinen - jimmymak@kth.se
