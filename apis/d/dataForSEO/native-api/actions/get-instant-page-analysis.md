# Get Instant Page Analysis with DataForSEO

Retrieves instant page analysis from DataForSEO.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/on_page/instant_pages.ai`
- **Base URL:** `https://api.dataforseo.com`
- **Official documentation:** [Get Instant Page Analysis](https://docs.dataforseo.com/v3/on_page-instant_pages/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | URL of the page to analyze. |
| `enable_javascript` | body | `boolean` | no | Enable JavaScript rendering for the page. |
| `custom_js` | body | `string` | no | Custom JavaScript code to execute. |
| `custom_user_agent` | body | `string` | no | Custom User-Agent header value. |
| `accept_language` | body | `string` | no | Language header value for accessing the website. |
