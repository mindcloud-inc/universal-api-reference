# Search Google SERP Light with HasData

Retrieves Google SERP Light results from HasData.

## Endpoint

- **Method:** `GET`
- **Path:** `/scrape/google-light/serp`
- **Base URL:** `https://api.hasdata.com`
- **Official documentation:** [Search Google SERP Light](https://docs.hasdata.com/apis/google-serp/serp-light)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `location` | query | `string` | no | Google canonical location for the search. |
| `num` | query | `string` | no | Number of results to return per page. |
| `q` | query | `string` | yes | Search term to send to Google. |
| `start` | query | `string` | no | Number of results to skip for pagination. |
