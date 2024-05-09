# Stardew Valley Fish Finder App

This project works as a fish finder for popular video game Stardew Valley, which is a game centered around operating a farm that has a day/night cycle, a seasonal cycle, and dynamic weather. It has a fishing mechanic as well. 

The availability of the fish to be caught in this game is based off of times of the day, seasons, weather, and location. Game time goes from 6AM to 2AM, and game seasons cycle from Spring to Fall.

Here's an example of a fish's availability:

```
Anchovy
[Ocean]
[Spring, Fall]
[Sun, Rain]
[6AM - 2AM]
```
This app allows the user to see what fish are available at a specific location, season, weather, and time. It has 3 pages.

## Pages

### Home Page
You can click on the button with the fishing emoji on it to return a list of all the individual fish stored in the app in console.log.

You can use the inputs on the home page to set the season, weather, and time desired. Times are all on the hour, as all the fish ranges are also on the hour. Location is specified on a different page, but its default setting is "Ocean". 

Press submit to see a list of all fish that fit the location, season, weather, and time criteria selected.

Each fish has a star button next to it. Clicking the star button favorites the fish by storing it in localStorage. Only one fish may be favorited at a time. The details of the favorited fish can be seen in the "Favorite" page.

### Set Location Page
This page allows the user to specify the user's fishing location by use of a drop down menu. Clicking the submit button confirms the user's choice. The Home page will now display the selected location.

### Favorite
This page contains the information of the fish that was favorited. Since the fish is saved to local storage, this information will persist across refreshes.

## Requirements
- Array: this project uses an array of objects in the file FishList.js
- React JSX Syntax: this projects uses JSX syntax to generate elements
- Form Elements and Interactive Events: this project has several forms (home page, set location, favoriting) that require the user to submit information that the app then registers to return info from FishList.js
- React Component: there are multiple components contained within the app
- React Module: FishList.js is a module that is used to return an array of Fish objects
- React Hook: UseState is used to dynamically update the fish display text. It can be found in component `FishDisplay`
- Storage: this app uses localStorage to store a favorite fish. You can see this in the `Favorite`, `ClearFavorite`, and `FavoriteDisplay` components
- React Routes: this app has three routes. `OptionsDisplay`, `SetLocation`, and `FavoriteDisplay`

## Questions
Q: What was the most satisfying part of this project?

A: Actually fitting the pieces together and seeing the entire app work as a whole. The search filtration was particularly satisfying to watch come together.

Q: If I had two more weeks, I would...

A: I would add more fish to the project, make the project more aesthetically pleasing, and make each fish its own individual page that lists its characteristics. I would also enable more favorites to be saved.

Q: What was the most useful thing we learned in this class?

A: The routes were incredibly useful, as were the hooks. Also map() has saved me more times than I can count.