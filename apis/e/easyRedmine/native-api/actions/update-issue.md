# Update Issue with Easy Redmine

Updates an existing issue in Easy Redmine.

## Endpoint

- **Method:** `PUT`
- **Path:** `/issues/:id.json`
- **Base URL:** `https://3f73561b8b.bigus-e5.easy8.com`
- **Official documentation:** [Update Issue](https://3f73561b8b.bigus-e5.easy8.com/easy_swagger.yml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the issue to update. |
| `issue` | body | `object` | yes | Issue payload to update. |
