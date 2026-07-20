# Get Selected HTML with WebScraping.AI

## Endpoint

- **Method:** `GET`
- **Path:** `/selected`
- **Base URL:** `https://api.webscraping.ai`
- **Official documentation:** [Get Selected HTML](https://webscraping.ai/docs#selected)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | URL of the webpage to fetch a selected HTML fragment from. |
| `selector` | query | `string` | yes | CSS selector for the HTML fragment to return. |
