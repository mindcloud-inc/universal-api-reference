# Extract HTTP Response Body with Automatic Data Extraction

Extracts an HTTP response body in Automatic Data Extraction.

## Endpoint

- **Method:** `POST`
- **Path:** `/extract`
- **Base URL:** `https://api.zyte.com/v1`
- **Official documentation:** [Extract HTTP Response Body](https://docs.zyte.com/zyte-api/usage/reference.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `httpResponseBody` | body | `string` | no | Return the Http Response Body field. |
| `url` | body | `string` | yes | Absolute URL to extract data from. |
