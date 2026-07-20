# Create Subfolder with Wistia

Creates a new subfolder in a Wistia folder.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/projects/:projectId/subfolders`
- **Base URL:** `https://api.wistia.com`
- **Official documentation:** [Create Subfolder](https://docs.wistia.com/reference/post_projects-projectid-subfolders)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `projectId` | path | `string` | yes |
| `name` | body | `string` | yes |
