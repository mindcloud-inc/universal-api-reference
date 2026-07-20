# Create Group with 5pm

Creates a new project group in 5pm.

## Endpoint

- **Method:** `POST`
- **Path:** `/service/post/projectsgroups/add`
- **Base URL:** `{workspaceUrl}/api/v2`
- **Official documentation:** [Create Group](https://www.5pmweb.com/help/api_docs.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group[name]` | query | `string` | yes | Name of the group to create. |
