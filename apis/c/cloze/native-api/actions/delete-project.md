# Delete Project with Cloze

Deletes a project from Cloze.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/projects/delete`
- **Base URL:** `https://api.cloze.com`
- **Official documentation:** [Delete Project](https://api.cloze.com/api-docs/#/paths/v1-projects-delete/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uniqueid` | query | `string` | yes | Project unique direct identifier or custom identifier. |
| `team` | query | `boolean` | no | Delete the team relation instead of the local relation. |
