# Get Projects with zipBoard

Retrieves projects from zipBoard.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects`
- **Base URL:** `https://app.zipboard.co/api/v1`
- **Official documentation:** [Get Projects](https://help.zipboard.co/article/178-api-for-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orgid` | body | `string` | yes | Organization ID to fetch projects for. |
| `orgid` | query | `string` | yes | — |
| `owner` | body | `boolean` | no | Return projects where the authenticated user is the owner. |
| `projectid` | body | `string` | no | Optional project ID filter. |
| `Role` | body | `string` | no | Optional role filter: owner, manager, or reviewer. |
