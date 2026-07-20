# Update Group with 5pm

Updates an existing project group in 5pm.

## Endpoint

- **Method:** `POST`
- **Path:** `/service/post/projectsgroups/update`
- **Base URL:** `{workspaceUrl}/api/v2`
- **Official documentation:** [Update Group](https://www.5pmweb.com/help/api_docs.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group[id]` | query | `string` | yes | Unique identifier of the group. |
| `group[name]` | query | `string` | yes | — |
