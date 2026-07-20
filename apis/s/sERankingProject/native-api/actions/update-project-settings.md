# Update Project Settings with SE Ranking Project

Updates an existing project in SE Ranking.

## Endpoint

- **Method:** `PUT`
- **Path:** `/sites/:site_id`
- **Base URL:** `https://api4.seranking.com`
- **Official documentation:** [Update Project Settings](https://seranking.com/api/project/project-management/#change-project-settings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `site_id` | path | `list<number>` | yes | Project site identifier from SE Ranking. |
| `url` | body | `string` | no | Project website URL. |
| `title` | body | `string` | no | Project name. |
