# Three-Day-Forecast

## Table of Contents

1. [Overview](#Overview)
2. [API Endpoint](#API-Endpoint)
3. [Request](#Request)
4. [Response](#Response)
	- Response Example
5. [Field Descriptions](#Field-Descriptions)
6. [Example Usage](#Example-Usage)
7. [Reference](#Reference)
8. [Conclusion](#Conclusion)

## Overview

## API Endpoint
```
GET /api/three-day-forecast
```

## Request

No specific parameters are required for the request. A simple GET request to the endpoint will return the forecast data.

### Example Request
```
GET /api/three-day-forecast HTTP/1.1
Host: example.com
```

## Response

The response is a JSON object containing the weather forecast for the next three days. Each day's forecast includes the weather description, maximum and minimum temperatures, wind speed, and a danger alert.

### Response Example
```
{
	"forecast": [ 
		{
			"Monday": { 
        		"description": "sunny",
        		"maxTemp": 22,
        		"minTemp": 20,
        		"windSpeed": 12,
        		"danger": false
        	}
    	},
    	{
    		"Tuesday": {
    			"description": "sunny",
        		"maxTemp": 22,
        		"minTemp": 20,
        		"windSpeed": 40,
        		"danger": true
        	}
    	},
    	{
    		"Wednesday": "null"
    	}
	]
}
```


## Field Descriptions

- **forecast:** An array containing the weather forecast for the next three days.
  - **Monday:** (Object) The weather forecast for Monday.
    - **description:** (String) A brief description of the weather (e.g., sunny, cloudy).
    - **maxTemp:** (Number) The maximum temperature in degrees Celsius.
    - **minTemp:** (Number) The minimum temperature in degrees Celsius.
    - **windSpeed:** (Number) The wind speed in kilometers per hour.
    - **danger:** (Boolean) Indicates whether there is a danger alert due to severe weather conditions.
  - **Tuesday:** (Object) The weather forecast for Tuesday.
    Similar fields as Monday.
  - **Wednesday:** (Object or String) The weather forecast for Wednesday. If no forecast is available, the value is "null".
 
## Example Usage

### Request
```
GET /api/three-day-forecast HTTP/1.1
Host: example.com
```

### Response
```
{
	"forecast": [ 
		{
			"Monday": { 
        		"description": "sunny",
        		"maxTemp": 22,
        		"minTemp": 20,
        		"windSpeed": 12,
        		"danger": false
        	}
    	},
    	{
    		"Tuesday": {
    			"description": "sunny",
        		"maxTemp": 22,
        		"minTemp": 20,
        		"windSpeed": 40,
        		"danger": true
        	}
    	},
    	{
    		"Wednesday": "null"
    	}
	]
}
```

## Reference

For needed thorough analysis of the project, please refer to the attached .pdf documenatation file.

## Conclusion
The Three-Day Forecast API provides essential weather information for the upcoming days, allowing users to prepare and plan accordingly. The API is straightforward to use, returning detailed weather data in a simple JSON format.
