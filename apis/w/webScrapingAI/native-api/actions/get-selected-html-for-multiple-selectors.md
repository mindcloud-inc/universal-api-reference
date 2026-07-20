# Get Selected HTML For Multiple Selectors with WebScraping.AI

## Endpoint

- **Method:** `GET`
- **Path:** `/selected-multiple`
- **Base URL:** `https://api.webscraping.ai`
- **Official documentation:** [Get Selected HTML For Multiple Selectors](https://webscraping.ai/docs#selected)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | URL of the webpage to fetch selected HTML fragments from. |
| `selectors` | query | `string<string>` | yes | CSS selectors for the HTML fragments to return. Send multiple values as a array. |
