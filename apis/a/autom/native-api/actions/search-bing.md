# Search Bing with Autom

Finds Bing search results in Autom.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/bing/search`
- **Base URL:** `https://api.autom.dev`
- **Official documentation:** [Search Bing](https://docs.autom.dev/bing-search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | The Bing query to run. |
| `cc` | query | `string` | no | Bing market code such as en-US. |
| `page` | query | `number` | no | Result page number to request. |
