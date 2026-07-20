# Search Indeed Listings with HasData

Retrieves Indeed listings from HasData.

## Endpoint

- **Method:** `GET`
- **Path:** `/scrape/indeed/listing`
- **Base URL:** `https://api.hasdata.com`
- **Official documentation:** [Search Indeed Listings](https://docs.hasdata.com/apis/indeed/listing)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | query | `string` | no | Indeed domain, such as www.indeed.com. |
| `keyword` | query | `string` | yes | Job keyword to search on Indeed. |
| `location` | query | `string` | yes | Location to search on Indeed. |
| `sort` | query | `string` | no | Sort order for Indeed results, such as date. |
| `start` | query | `number` | no | Result offset for Indeed pagination. |
