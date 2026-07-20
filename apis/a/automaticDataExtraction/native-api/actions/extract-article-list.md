# Extract Article List with Automatic Data Extraction

Extracts article list data in Automatic Data Extraction.

## Endpoint

- **Method:** `POST`
- **Path:** `/extract`
- **Base URL:** `https://api.zyte.com/v1`
- **Official documentation:** [Extract Article List](https://docs.zyte.com/zyte-api/usage/reference.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `articleList` | body | `string` | no | Return the Article List field. |
| `url` | body | `string` | yes | Absolute URL to extract data from. |
