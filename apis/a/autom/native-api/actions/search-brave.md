# Search Brave with Autom

Finds Brave search results in Autom.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/brave/search`
- **Base URL:** `https://api.autom.dev`
- **Official documentation:** [Search Brave](https://docs.autom.dev/brave-search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | The Brave query to run. |
| `page` | query | `number` | no | Result page number to request. |
