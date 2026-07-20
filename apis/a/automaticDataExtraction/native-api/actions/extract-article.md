# Extract Article with Automatic Data Extraction

Extracts article data in Automatic Data Extraction.

## Endpoint

- **Method:** `POST`
- **Path:** `/extract`
- **Base URL:** `https://api.zyte.com/v1`
- **Official documentation:** [Extract Article](https://docs.zyte.com/zyte-api/usage/reference.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `article` | body | `string` | no | Return the Article field. |
| `url` | body | `string` | yes | Absolute URL to extract data from. |
