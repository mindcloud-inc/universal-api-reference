# List Country Cities with Scrapi

Retrieves supported proxy cities for a country from Scrapi.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/countries/{countryKey}/cities`
- **Base URL:** `https://api.scrapi.tech`
- **Official documentation:** [List Country Cities](https://scrapi.tech/docs/api_details/v1_scrape)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `countryKey` | path | `string` | yes | Country key used to look up supported cities. |
