# Add Keywords to Project with SE Ranking Project

Adds keywords to an existing SE Ranking project.

## Endpoint

- **Method:** `POST`
- **Path:** `/sites/:site_id/keywords`
- **Base URL:** `https://api4.seranking.com`
- **Official documentation:** [Add Keywords to Project](https://seranking.com/api/project/project-management/#add-queries-to-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `site_id` | path | `list<number>` | yes | Project site identifier from SE Ranking. |
| `keyword` | body | `string` | yes | — |
