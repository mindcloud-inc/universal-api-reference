# Get Competitor Keyword Positions with SE Ranking Project

Retrieves competitor keyword rankings from SE Ranking.

## Endpoint

- **Method:** `GET`
- **Path:** `/competitors/:competitor_id/positions`
- **Base URL:** `https://api4.seranking.com`
- **Official documentation:** [Get Competitor Keyword Positions](https://seranking.com/api/project/competitors/#get-competitor-keyword-positions)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `competitor_id` | path | `number` | yes |
| `date_from` | query | `date` | no |
| `date_to` | query | `date` | no |
| `site_engine_id` | query | `number` | no |
| `with_serp_features` | query | `number` | no |
