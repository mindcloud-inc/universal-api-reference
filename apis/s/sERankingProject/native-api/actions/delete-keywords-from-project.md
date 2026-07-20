# Delete Keywords from Project with SE Ranking Project

Deletes project keywords from SE Ranking.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/sites/:site_id/keywords`
- **Base URL:** `https://api4.seranking.com`
- **Official documentation:** [Delete Keywords from Project](https://seranking.com/api/project/project-management/#delete-keywords)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `site_id` | path | `list<number>` | yes | Project site identifier from SE Ranking. |
| `keywords_ids[]` | query | `array<number>` | yes | Array of keyword IDs to delete. |
