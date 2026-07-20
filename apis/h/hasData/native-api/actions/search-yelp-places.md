# Search Yelp Places with HasData

Retrieves Yelp place results from HasData.

## Endpoint

- **Method:** `GET`
- **Path:** `/scrape/yelp/search`
- **Base URL:** `https://api.hasdata.com`
- **Official documentation:** [Search Yelp Places](https://docs.hasdata.com/apis/yelp/search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | query | `string` | no | Yelp domain, such as www.yelp.com. |
| `keyword` | query | `string` | yes | Search keyword for Yelp businesses. |
| `location` | query | `string` | yes | Location to search for Yelp businesses. |
| `start` | query | `string` | no | Result offset for Yelp pagination. |
