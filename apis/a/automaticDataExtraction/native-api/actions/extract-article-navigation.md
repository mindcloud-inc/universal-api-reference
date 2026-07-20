# Extract Article Navigation with Automatic Data Extraction

Extracts article navigation data in Automatic Data Extraction.

## Endpoint

- **Method:** `POST`
- **Path:** `/extract`
- **Base URL:** `https://api.zyte.com/v1`
- **Official documentation:** [Extract Article Navigation](https://docs.zyte.com/zyte-api/usage/reference.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `articleNavigation` | body | `string` | no | Return the Article Navigation field. |
| `url` | body | `string` | yes | Absolute URL to extract data from. |
