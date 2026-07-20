# Get Facebook Profile with Scrape Creators

Retrieves a Facebook profile from Scrape Creators.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/facebook/profile`
- **Base URL:** `https://api.scrapecreators.com`
- **Official documentation:** [Get Facebook Profile](https://docs.scrapecreators.com/v1/facebook/profile/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | Facebook profile URL |
| `get_business_hours` | query | `boolean` | no | Include business hours when available |
