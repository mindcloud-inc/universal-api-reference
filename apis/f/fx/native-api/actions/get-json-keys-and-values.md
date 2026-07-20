# Get JSON Keys and Values with 1001fx

Retrieves JSON object keys and values.

## Endpoint

- **Method:** `POST`
- **Path:** `/data/getjsonkeysandvalues`
- **Base URL:** `https://api.1001fx.com`
- **Official documentation:** [Get JSON Keys and Values](https://1001fx.com/functions/getjsonkeysandvalues)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `json` | body | `object` | no | JSON object to inspect. |
| `jsonString` | body | `string` | no | JSON string to inspect when not passing a JSON object. |
