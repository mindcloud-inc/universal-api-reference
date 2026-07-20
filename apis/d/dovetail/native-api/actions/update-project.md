# Update Project with Dovetail

Updates an existing project in Dovetail.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/projects/:projectId`
- **Base URL:** `https://dovetail.com/api`
- **Official documentation:** [Update Project](https://developers.dovetail.com/reference/patch_v1-projects-projectid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | — |
| `title` | body | `string` | no | Project title. |
