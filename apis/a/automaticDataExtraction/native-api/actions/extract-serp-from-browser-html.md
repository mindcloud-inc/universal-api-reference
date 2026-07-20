# Extract SERP From Browser HTML with Automatic Data Extraction

Extracts SERP data from browser HTML in Automatic Data Extraction.

## Endpoint

- **Method:** `POST`
- **Path:** `/extract`
- **Base URL:** `https://api.zyte.com/v1`
- **Official documentation:** [Extract SERP From Browser HTML](https://docs.zyte.com/zyte-api/usage/reference.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `browserHtml` | body | `string` | no | Return the Browser Html field. |
| `url` | body | `string` | yes | Absolute URL to extract data from. |
