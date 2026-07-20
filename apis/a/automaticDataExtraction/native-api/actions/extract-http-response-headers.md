# Extract HTTP Response Headers with Automatic Data Extraction

Extracts HTTP response headers in Automatic Data Extraction.

## Endpoint

- **Method:** `POST`
- **Path:** `/extract`
- **Base URL:** `https://api.zyte.com/v1`
- **Official documentation:** [Extract HTTP Response Headers](https://docs.zyte.com/zyte-api/usage/reference.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `httpResponseHeaders` | body | `string` | no | Return the Http Response Headers field. |
| `url` | body | `string` | yes | Absolute URL to extract data from. |
