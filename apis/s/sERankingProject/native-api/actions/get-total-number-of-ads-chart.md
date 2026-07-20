# Get Total Number Of Ads Chart with SE Ranking Project

Retrieves keyword ad counts by date from SE Ranking.

## Endpoint

- **Method:** `GET`
- **Path:** `/sites/:site_id/ads`
- **Base URL:** `https://api4.seranking.com`
- **Official documentation:** [Get Total Number Of Ads Chart](https://seranking.com/api/project/project-management/#total-number-of-ads-chart)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `date_from` | query | `date` | yes |
| `date_to` | query | `date` | yes |
| `keywords_ids[]` | query | `array<number>` | no |
| `site_engine_ids[]` | query | `array<number>` | no |
| `site_id` | path | `list<number>` | yes |
