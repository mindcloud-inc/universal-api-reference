# Retrieve Content with Olostep

Retrieves content by retrieve ID from Olostep.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/retrieve`
- **Base URL:** `https://api.olostep.com`
- **Official documentation:** [Retrieve Content](https://docs.olostep.com/api-reference/retrieve)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `retrieve_id` | query | `string` | yes | Retrieve ID from a crawl page, scrape, or batch item response. |
| `formats[]` | query | `array<string>` | no | Optional formats to return. Choose one or more of html, markdown, or json. If omitted, all available formats are returned. Send multiple values as a array. |
