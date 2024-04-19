# Google Satellite API

This repository demonstrates how to integrate Google's Satellite API into web applications to display high-resolution satellite imagery. It provides a practical guide on API setup, example usage, and leveraging satellite images for various applications.

## Prerequisites

- A Google Cloud account
- An API key with access to Google Maps and Satellite services

## Installation

### Setting up the API Key

1. Visit the [Google Cloud Platform Console](https://console.cloud.google.com/).
2. Create a new project or select an existing project.
3. Navigate to "APIs & Services" > "Credentials".
4. Click "Create credentials" and select "API key". Ensure that your API key is enabled for the Google Maps JavaScript API and has permission to access satellite imagery.

## Basic Usage Examples

### Displaying Satellite Imagery

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Satellite Map</title>
    <script src="https://maps.googleapis.com/maps/api/js?key=YOUR_API_KEY&callback=initMap"
    async defer></script>
    <script>
      function initMap() {
        var location = {lat: -34.397, lng: 150.644};
        var map = new google.maps.Map(document.getElementById('map'), {
          zoom: 10,
          center: location,
          mapTypeId: 'satellite'
        });
        map.setTilt(45);
      }
    </script>
  </head>
  <body>
    <div id="map" style="height: 400px; width: 100%;"></div>
  </body>
</html>
```

## Contributing

Contributors who are interested in enhancing the examples, improving documentation, or adding new features related to satellite imagery are welcome. Please fork the repository, create your feature branch, and submit a pull request.

## License

This project is licensed under the MIT License. See the LICENSE file for more details.
