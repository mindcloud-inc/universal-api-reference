# Update Version with Easy Redmine

Updates an existing version in Easy Redmine.

## Endpoint

- **Method:** `PUT`
- **Path:** `/versions/:id.json`
- **Base URL:** `https://3f73561b8b.bigus-e5.easy8.com`
- **Official documentation:** [Update Version](https://3f73561b8b.bigus-e5.easy8.com/easy_swagger.yml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the version to update. |
| `version` | body | `object` | yes | Version payload to update. |
