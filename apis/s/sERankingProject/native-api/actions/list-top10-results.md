# List Top 10 Results with SE Ranking Project

Retrieves top 10 ranking results from SE Ranking.

## Endpoint

- **Method:** `GET`
- **Path:** `/competitors/top10/:site_id`
- **Base URL:** `https://api4.seranking.com`
- **Official documentation:** [List Top 10 Results](https://seranking.com/api/project/competitors/#get-top-10-results)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `date` | query | `string` | yes |
| `keyword_id` | query | `number` | yes |
| `site_engine_id` | query | `number` | yes |
| `site_id` | path | `list<number>` | yes |
