# Run Position Check with SE Ranking Project

Triggers a keyword position check in SE Ranking.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/sites/:site_id/recheck`
- **Base URL:** `https://api4.seranking.com`
- **Official documentation:** [Run Position Check](https://seranking.com/api/project/project-management/#run-position-check)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `site_id` | path | `list<number>` | yes |
| `keywords[]` | body | `array<object>` | no |
| `site_engine_id` | body | `number` | no |
