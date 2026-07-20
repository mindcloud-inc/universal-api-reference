# Search Google Events with HasData

Retrieves Google Events results from HasData.

## Endpoint

- **Method:** `GET`
- **Path:** `/scrape/google/events`
- **Base URL:** `https://api.hasdata.com`
- **Official documentation:** [Search Google Events](https://docs.hasdata.com/apis/google-serp/events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `location` | query | `string` | no | Google canonical location for the event search. |
| `q` | query | `string` | yes | Search term for Google Events. |
| `start` | query | `number` | no | Result offset for pagination. |
