# Get prompts by target with SE Ranking Data

Retrieves prompts by target from SE Ranking Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/ai-search/prompts-by-target`
- **Base URL:** `https://api.seranking.com/v1`
- **Official documentation:** [Get prompts by target](https://seranking.com/api/data/ai-search/#get-prompts-by-target)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end_date` | query | `string` | no | End date in YYYY-MM-DD format. |
| `engine` | query | `list<string>` | yes | Engine identifier (for example: chatgpt). Accepted values: `ai_overview`, `chatgpt`. |
| `fields` | query | `string` | no | Comma-separated fields to include. |
| `scope` | query | `list<string>` | yes | Analysis scope (for example: domain). Accepted values: `base_domain`, `domain`, `exact_url`, `path`, `subdomain`. |
| `sort` | query | `string` | no | Comma-separated sort fields with direction (for example: date:desc). |
| `source` | query | `string` | yes | Regional source code (for example: us). |
| `start_date` | query | `string` | no | Start date in YYYY-MM-DD format. |
| `target` | query | `string` | yes | Target domain or URL (for example: seranking.com). |
