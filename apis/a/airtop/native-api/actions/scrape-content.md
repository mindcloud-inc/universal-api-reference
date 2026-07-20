# Scrape Content with Airtop

Scrapes content from an Airtop window.

## Endpoint

- **Method:** `POST`
- **Path:** `/sessions/:sessionId/windows/:windowId/scrape-content`
- **Base URL:** `https://api.airtop.ai/api/v1`
- **Official documentation:** [Scrape Content](https://docs.airtop.ai/api-reference/airtop-api/windows/scrape-content)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `sessionId` | path | `string` | yes |
| `windowId` | path | `string` | yes |
