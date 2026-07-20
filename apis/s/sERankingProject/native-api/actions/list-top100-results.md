# List Top 100 Results with SE Ranking Project

Retrieves top 100 ranking results from SE Ranking.

## Endpoint

- **Method:** `GET`
- **Path:** `/competitors/top100/:site_id`
- **Base URL:** `https://api4.seranking.com`
- **Official documentation:** [List Top 100 Results](https://seranking.com/api/project/competitors/#get-top-100-results)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `date` | query | `string` | yes |
| `keyword_id` | query | `number` | yes |
| `site_engine_id` | query | `number` | yes |
| `site_id` | path | `list<number>` | yes |
| `top` | query | `number` | no |
