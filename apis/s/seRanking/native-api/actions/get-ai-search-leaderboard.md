# Get AI search leaderboard with SE Ranking Data

Retrieves the AI search leaderboard from SE Ranking Data.

## Endpoint

- **Method:** `POST`
- **Path:** `/ai-search/overview/leaderboard`
- **Base URL:** `https://api.seranking.com/v1`
- **Official documentation:** [Get AI search leaderboard](https://seranking.com/api/data/ai-search/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `competitors` | body | `list<object>` | yes | Competitor objects array with target and optional brand. |
| `engines` | body | `list<string>` | yes | One or more engines (for example: chatgpt, ai_overview). Accepted values: `ai_overview`, `chatgpt`. |
| `primary.brand` | body | `string` | no | Optional primary brand label. |
| `primary.target` | body | `string` | yes | Primary target domain/URL. |
| `scope` | body | `list<string>` | yes | Scope value (for example: domain). Accepted values: `base_domain`, `domain`, `exact_url`, `path`, `subdomain`. |
| `source` | body | `string` | yes | Regional source code (for example: us). |
