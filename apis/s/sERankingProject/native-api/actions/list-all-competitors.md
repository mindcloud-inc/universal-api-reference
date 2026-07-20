# List All Competitors with SE Ranking Project

Retrieves top-ranked competitor domains from SE Ranking.

## Endpoint

- **Method:** `GET`
- **Path:** `/competitors/all/:site_id`
- **Base URL:** `https://api4.seranking.com`
- **Official documentation:** [List All Competitors](https://seranking.com/api/project/competitors/#get-all-competitors)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `date` | query | `string` | yes |
| `group_id` | query | `number` | no |
| `site_engine_id` | query | `number` | yes |
| `site_id` | path | `list<number>` | yes |
| `tags[]` | query | `array<number>` | no |
