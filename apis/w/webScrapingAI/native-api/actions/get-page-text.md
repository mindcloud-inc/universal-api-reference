# Get Page Text with WebScraping.AI

## Endpoint

- **Method:** `GET`
- **Path:** `/text`
- **Base URL:** `https://api.webscraping.ai`
- **Official documentation:** [Get Page Text](https://webscraping.ai/docs#text)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | Target webpage URL |
| `text_format` | query | `string` | no | Format of the text response: plain, json, or xml |
| `return_links` | query | `boolean` | no | Include links in the JSON response |
