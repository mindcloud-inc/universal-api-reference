# Get Markdownify Status with ScrapeGraphAI

Retrieves Markdownify request status from ScrapeGraphAI.

## Endpoint

- **Method:** `GET`
- **Path:** `/markdownify/:request_id`
- **Base URL:** `https://api.scrapegraphai.com/v1`
- **Official documentation:** [Get Markdownify Status](https://docs.scrapegraphai.com/api-reference/endpoint/markdownify/get-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request_id` | path | `string` | yes | Markdownify request ID to retrieve. |
