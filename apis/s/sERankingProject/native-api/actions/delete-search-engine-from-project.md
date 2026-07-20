# Delete Search Engine From Project with SE Ranking Project

Deletes a project search engine from SE Ranking.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/sites/:site_id/search-engines/:site_engine_id`
- **Base URL:** `https://api4.seranking.com`
- **Official documentation:** [Delete Search Engine From Project](https://seranking.com/api/project/project-management/#delete-search-engine-from-project)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `site_engine_id` | path | `number` | yes |
| `site_id` | path | `list<number>` | yes |
