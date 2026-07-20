# Update Search Engine in Project with SE Ranking Project

Updates a project search engine in SE Ranking.

## Endpoint

- **Method:** `PUT`
- **Path:** `/sites/:site_id/search-engines/:site_engine_id`
- **Base URL:** `https://api4.seranking.com`
- **Official documentation:** [Update Search Engine in Project](https://seranking.com/api/project/project-management/#change-search-engine-in-project)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `lang_code` | body | `string` | no |
| `region_id` | body | `number` | no |
| `site_engine_id` | path | `number` | yes |
| `site_id` | path | `list<number>` | yes |
