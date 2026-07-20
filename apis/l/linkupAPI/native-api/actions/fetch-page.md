# Fetch Page with LinkupAPI

Retrieves a single webpage by URL from LinkupAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/fetch`
- **Base URL:** `https://api.linkup.so/v1`
- **Official documentation:** [Fetch Page](https://docs.linkup.so/pages/documentation/api-reference/endpoint/post-fetch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | The URL of the webpage to fetch. |
| `renderJs` | body | `boolean` | no | Render the page's JavaScript before extracting content. |
| `includeRawHtml` | body | `boolean` | no | Include the raw HTML in the response. |
| `extractImages` | body | `boolean` | no | Extract images from the fetched page. |
