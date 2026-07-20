# Update Project with Easy Redmine

Updates an existing project in Easy Redmine.

## Endpoint

- **Method:** `PUT`
- **Path:** `/projects/:id.json`
- **Base URL:** `https://3f73561b8b.bigus-e5.easy8.com`
- **Official documentation:** [Update Project](https://3f73561b8b.bigus-e5.easy8.com/easy_swagger.yml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the project to update. |
| `project` | body | `object` | yes | Project payload to update. |
