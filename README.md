# weather_forecast_api

WeatherForecastApi - JavaScript client for weather_forecast_api
This is the swagger definition of the weather forecast API. For more info contact sdimopoulos@irisweb.gr
This SDK is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: 1.0.0
- Package version: 1.0.0
- Build package: io.swagger.codegen.languages.JavascriptClientCodegen

## Installation

### For [Node.js](https://nodejs.org/)

#### npm

To publish the library as a [npm](https://www.npmjs.com/),
please follow the procedure in ["Publishing npm packages"](https://docs.npmjs.com/getting-started/publishing-npm-packages).

Then install it via:

```shell
npm install weather_forecast_api --save
```

##### Local development

To use the library locally without publishing to a remote npm registry, first install the dependencies by changing 
into the directory containing `package.json` (and this README). Let's call this `JAVASCRIPT_CLIENT_DIR`. Then run:

```shell
npm install
```

Next, [link](https://docs.npmjs.com/cli/link) it globally in npm with the following, also from `JAVASCRIPT_CLIENT_DIR`:

```shell
npm link
```

Finally, switch to the directory you want to use your weather_forecast_api from, and run:

```shell
npm link /path/to/<JAVASCRIPT_CLIENT_DIR>
```

You should now be able to `require('weather_forecast_api')` in javascript files from the directory you ran the last 
command above from.

#### git
#
If the library is hosted at a git repository, e.g.
https://github.com/YOUR_USERNAME/weather_forecast_api
then install it via:

```shell
    npm install YOUR_USERNAME/weather_forecast_api --save
```

### For browser

The library also works in the browser environment via npm and [browserify](http://browserify.org/). After following
the above steps with Node.js and installing browserify with `npm install -g browserify`,
perform the following (assuming *main.js* is your entry file, that's to say your javascript file where you actually 
use this library):

```shell
browserify main.js > bundle.js
```

Then include *bundle.js* in the HTML pages.

### Webpack Configuration

Using Webpack you may encounter the following error: "Module not found: Error:
Cannot resolve module", most certainly you should disable AMD loader. Add/merge
the following section to your webpack config:

```javascript
module: {
  rules: [
    {
      parser: {
        amd: false
      }
    }
  ]
}
```

## Getting Started

Please follow the [installation](#installation) instruction and execute the following JS code:

```javascript
var WeatherForecastApi = require('weather_forecast_api');

var defaultClient = WeatherForecastApi.ApiClient.instance;

// Configure API key authorization: api_key
var api_key = defaultClient.authentications['api_key'];
api_key.apiKey = "YOUR API KEY"
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix['token'] = "Token"

var api = new WeatherForecastApi.CityApi()

var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
api.getAllCityInfo(callback);

```

## Documentation for API Endpoints

All URIs are relative to *https://forecast-api.irisweb.gr/v1*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*WeatherForecastApi.CityApi* | [**getAllCityInfo**](docs/CityApi.md#getAllCityInfo) | **GET** /city | Get a list of all cities
*WeatherForecastApi.CityApi* | [**getCityInfo**](docs/CityApi.md#getCityInfo) | **GET** /city/{cityId} | Find city by ID


## Documentation for Models

 - [WeatherForecastApi.ApiResponse](docs/ApiResponse.md)
 - [WeatherForecastApi.City](docs/City.md)
 - [WeatherForecastApi.CityCoords](docs/CityCoords.md)
 - [WeatherForecastApi.ForecastInfo](docs/ForecastInfo.md)
 - [WeatherForecastApi.ForecastInfoHumidity](docs/ForecastInfoHumidity.md)
 - [WeatherForecastApi.ForecastInfoPressure](docs/ForecastInfoPressure.md)
 - [WeatherForecastApi.ForecastInfoTemperature](docs/ForecastInfoTemperature.md)


## Documentation for Authorization


### api_key

- **Type**: API key
- **API key parameter name**: token
- **Location**: HTTP header
