# de2023-Mapping system

## New mapping system for recording data on indigenous traditional practices   


<!DOCTYPE html>
<html>
  
  <head>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/0.6.1/p5.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/0.6.1/addons/p5.dom.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/0.6.1/addons/p5.sound.min.js"></script>
    <script src="https://unpkg.com/mappa-mundi@0.0.5/dist/mappa.js" type="text/javascript"></script>
    
    <script async src="https://maps.googleapis.com/maps/api/js?key=AIzaSyDryJwWTPoG6j-yY63l-ZGWuvy2lSYlTB4&callback=initMap">
</script>
    
    <link rel="stylesheet" type="text/css" href="style.css">
    <meta charset="utf-8" />
  
  </head>
  
  <body>
    <script src="sketch.js"></script>
  </body>
  
</html>


 
// API Key for Google Maps. Get one here:
// https://developers.google.com/maps/web/
const key = 'AIzaSyDryJwWTPoG6j-yY63l-ZGWuvy2lSYlTB4';

// Style for Google Maps. This is optional. More information here:
// https://mapstyle.withgoogle.com/
const style = [{
  elementType: 'geometry',
  stylers: [{
    color: '#000000',
  }],
}, {
  elementType: 'labels.text.fill',
  stylers: [{
    color: '#746855',
    'visibility': 'off'
  }],
}, {
  elementType: 'labels.text.stroke',
  stylers: [{
    color: '#242f3e',
    'visibility': 'off'
  }],
}, {
  'featureType': 'administrative.land_parcel',
  stylers: [{
    'visibility': 'off'
  }]
}, {
  'featureType': 'administrative.locality',
  elementType: 'labels.text.fill',
  stylers: [{
    color: '#FFFFFF',
    'visibility': 'off'
  }]
}, {
  'featureType': 'administrative.neighborhood',
  stylers: [{
    'visibility': 'off'
  }]
}, {
  'featureType': 'poi',
  elementType: 'labels.text',
  stylers: [{
    'visibility': 'off'
  }]
}, {
  'featureType': 'poi',
  elementType: 'labels.text.fill',
  stylers: [{
    color: '#d59563',
    'visibility': 'off'
  }]
}, {
  'featureType': 'poi.park',
  elementType: 'geometry',
  stylers: [{
    color: '#263c3f'
  }]
}, {
  'featureType': 'poi.park',
  elementType: 'labels.text.fill',
  stylers: [{
    color: '#6b9a76',
    'visibility': 'off'
  }]
}, {
  'featureType': 'road',
  stylers: [{
    'visibility': 'off'
  }]
}, {
  'featureType': 'road',
  elementType: 'geometry',
  stylers: [{
    color: '#38414e'
  }]
}, {
  'featureType': 'road',
  elementType: 'geometry.stroke',
  stylers: [{
    color: '#212a37'
  }]
}, {
  'featureType': 'road',
  elementType: 'labels',
  stylers: [{
    'visibility': 'off'
  }]
}, {
  'featureType': 'road',
  elementType: 'labels.text.fill',
  stylers: [{
    color: '#9ca5b3'
  }]
}, {
  'featureType': 'road.highway',
  elementType: 'geometry',
  stylers: [{
    color: '#746855'
  }]
}, {
  'featureType': 'road.highway',
  elementType: 'geometry.stroke',
  stylers: [{
    color: '#1f2835'
  }]
}, {
  'featureType': 'road.highway',
  elementType: 'labels.text.fill',
  stylers: [{
    color: '#f3d19c',
    'visibility': 'off'
  }]
}, {
  'featureType': 'transit',
  elementType: 'geometry',
  stylers: [{
    color: '#2f3948'
  }]
}, {
  'featureType': 'transit.station',
  elementType: 'labels.text.fill',
  stylers: [{
    color: '#d59563',
    'visibility': 'off'
  }]
}, {
  'featureType': 'water',
  elementType: 'geometry',
  stylers: [{
    color: '#17263c'
  }]
}, {
  'featureType': 'water',
  elementType: 'labels.text',
  stylers: [{
    'visibility': 'off'
  }]
}, {
  'featureType': 'water',
  elementType: 'labels.text.fill',
  stylers: [{
    color: '#515c6d'
  }]
}, {
  'featureType': 'water',
  elementType: 'labels.text.stroke',
  stylers: [{
    color: '#17263c'
  }]
}];

// Options for map
const options = {
  lat: -38.841460010161384,
  lng: -69.735082761222,
  zoom: 10,
  styles: style,
};

// Create an instance of Google
const mappa = new Mappa('Google', key);

let myMap;


function setup() {
  //canvas = createCanvas(640, 580).parent('canvasContainer');
  canvas = createCanvas(windowWidth,windowHeight);

  // Create a tile map and overlay the canvas on top.
  myMap = mappa.tileMap(options);
  myMap.overlay(canvas);
 
}

function draw() {
  
}

