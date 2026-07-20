# Search JSON with 1001fx

Finds matching key-value pairs in a JSON object.

## Endpoint

- **Method:** `POST`
- **Path:** `/data/deepsearchjson`
- **Base URL:** `https://api.1001fx.com`
- **Official documentation:** [Search JSON](https://1001fx.com/functions/deepsearchjson)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `comparison` | body | `string` | yes | Comparison mode used for the search. |
| `json` | body | `object` | no | JSON object to search. |
| `jsonString` | body | `string` | no | JSON string to search when not passing a JSON object. |
| `scope` | body | `string` | no | Scope to search within. |
| `searchString` | body | `string` | yes | String to search for in the JSON payload. |
