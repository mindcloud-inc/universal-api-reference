# Add Search Engine To Project with SE Ranking Project

Creates a project search engine in SE Ranking.

## Endpoint

- **Method:** `POST`
- **Path:** `/sites/:site_id/search-engines`
- **Base URL:** `https://api4.seranking.com`
- **Official documentation:** [Add Search Engine To Project](https://seranking.com/api/project/project-management/#add-search-engine-to-project)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `lang_code` | body | `string` | no |
| `region_id` | body | `number` | no |
| `search_engine_id` | body | `number` | yes |
| `site_id` | path | `list<number>` | yes |
