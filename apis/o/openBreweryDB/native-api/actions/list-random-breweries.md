# List Random Breweries with Open Brewery DB

Retrieves random breweries from Open Brewery DB.

## Endpoint

- **Method:** `GET`
- **Path:** `/breweries/random`
- **Base URL:** `https://api.openbrewerydb.org/v1`
- **Official documentation:** [List Random Breweries](https://www.openbrewerydb.org/documentation#random-brewery)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `size` | query | `number` | yes | Number of random breweries to return. Use 2-50 for a list response; maximum is 50. |
