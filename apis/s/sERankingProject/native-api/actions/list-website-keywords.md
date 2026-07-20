# List Website Keywords with SE Ranking Project

Retrieves project keywords and basic statistics from SE Ranking.

## Endpoint

- **Method:** `GET`
- **Path:** `/sites/:site_id/keywords`
- **Base URL:** `https://api4.seranking.com`
- **Official documentation:** [List Website Keywords](https://seranking.com/api/project/project-management/#website-keyword-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `site_id` | path | `list<number>` | yes | Project site identifier from SE Ranking. |
