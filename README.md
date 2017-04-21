TRULLOW (ITC 2017)
========

## First Time Installation
1) Download and install node.js [https://nodejs.org/en/]
- You can check if the installation was successful with the commands `node -v` and `npm -v`
- The commands print the version number
2) Install Bower with `npm install -g bower`

## Daily Workflow
1) `git pull`
2) `npm install`
3) `bower install`
4) Run server

## How to Run Server
- Through IDE: Run > Run [If this doesn't work, try 'Edit Configurations' > JavaScript file: bin/www]
- Through Command Line: `node bin/www`
- App will be running on port '3000'. Check out app at: 'localhost:3000' in the browser

## Features

### Weather

### School
`school.js` contains the createSchoolsCtrl() function called from the home page to display the places labeled as "school" or "university" on the map. The Places library from the Google Maps API is used to make a search for the nearby places within 8000 meters from the given current map's viewpoint. 

```js
var service = new google.maps.places.PlacesService(map);

service.nearbySearch({
    location: map.getCenter(),
    radius: 8000,
    type: ['school', 'university']
}, function(results, status) {
    // if successful, create marker for each result
    if (status === google.maps.places.PlacesServiceStatus.OK) {
        for (var i = 0; i < results.length; i++) {
            createMarker(results[i], icon);
        }
    }
});
```

### Crime

### Amenities

### Transportation
