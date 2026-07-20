# Get prompts by brand with SE Ranking Data

Retrieves prompts by brand from SE Ranking Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/ai-search/prompts-by-brand`
- **Base URL:** `https://api.seranking.com/v1`
- **Official documentation:** [Get prompts by brand](https://seranking.com/api/data/ai-search/#get-prompts-by-brand)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `brand` | query | `string` | yes | Brand identifier or name. |
| `end_date` | query | `string` | no | End date in YYYY-MM-DD format. |
| `engine` | query | `list<string>` | yes | Engine identifier (for example: chatgpt). Accepted values: `ai_overview`, `chatgpt`. |
| `fields` | query | `string` | no | Comma-separated fields to include. |
| `sort` | query | `string` | no | Comma-separated sort fields with direction (for example: date:desc). |
| `source` | query | `string` | yes | Regional source code (for example: us). |
| `start_date` | query | `string` | no | Start date in YYYY-MM-DD format. |
