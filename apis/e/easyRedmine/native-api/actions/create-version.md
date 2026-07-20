# Create Version with Easy Redmine

Creates a new version in an Easy Redmine project.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:projectId/versions.json`
- **Base URL:** `https://3f73561b8b.bigus-e5.easy8.com`
- **Official documentation:** [Create Version](https://3f73561b8b.bigus-e5.easy8.com/easy_swagger.yml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `number` | yes | ID of the project to create the version in. |
| `version` | body | `object` | yes | Version payload to create. |
