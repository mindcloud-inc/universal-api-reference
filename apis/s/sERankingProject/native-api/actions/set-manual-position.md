# Set Manual Position with SE Ranking Project

Updates a keyword's ranking position in SE Ranking.

## Endpoint

- **Method:** `PUT`
- **Path:** `/sites/:site_id/position`
- **Base URL:** `https://api4.seranking.com`
- **Official documentation:** [Set Manual Position](https://seranking.com/api/project/project-management/#set-manual-position)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `date` | body | `string` | yes |
| `keyword_id` | body | `number` | yes |
| `position` | body | `number` | yes |
| `site_engine_id` | body | `number` | yes |
| `site_id` | path | `list<number>` | yes |
