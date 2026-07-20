# Update Group with Easy Redmine

Updates an existing group in Easy Redmine.

## Endpoint

- **Method:** `PUT`
- **Path:** `/groups/:id.json`
- **Base URL:** `https://3f73561b8b.bigus-e5.easy8.com`
- **Official documentation:** [Update Group](https://3f73561b8b.bigus-e5.easy8.com/easy_swagger.yml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the group to update. |
| `group` | body | `object` | yes | Group payload to update. |
