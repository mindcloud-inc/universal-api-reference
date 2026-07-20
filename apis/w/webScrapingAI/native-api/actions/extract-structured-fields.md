# Extract Structured Fields with WebScraping.AI

## Endpoint

- **Method:** `GET`
- **Path:** `/ai/fields`
- **Base URL:** `https://api.webscraping.ai`
- **Official documentation:** [Extract Structured Fields](https://webscraping.ai/docs#ai-fields)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | URL of the webpage to extract structured fields from. |
| `fields` | query | `object` | yes | Field-to-description object used to tell WebScraping.AI what structured values to extract. |
