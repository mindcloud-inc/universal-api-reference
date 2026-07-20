# Get AI search overview with SE Ranking Data

Retrieves AI search overview data from SE Ranking Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/ai-search/overview/by-engine/time-series`
- **Base URL:** `https://api.seranking.com/v1`
- **Official documentation:** [Get AI search overview](https://seranking.com/api/data/ai-search/#overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end_date` | query | `string` | no | End date in YYYY-MM-DD format. |
| `engine` | query | `list<string>` | yes | Engine identifier (for example: chatgpt). Accepted values: `ai_overview`, `chatgpt`. |
| `scope` | query | `list<string>` | yes | Analysis scope: domain, base_domain, subdomain, exact_url, or path. Accepted values: `base_domain`, `domain`, `exact_url`, `path`, `subdomain`. |
| `source` | query | `string` | yes | Regional source code (for example: us). |
| `start_date` | query | `string` | no | Start date in YYYY-MM-DD format. |
| `target` | query | `string` | yes | Target domain or URL (for example: seranking.com). |
