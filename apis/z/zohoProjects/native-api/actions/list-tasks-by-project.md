# List Tasks By Project with Zoho Projects

Retrieves tasks from a Zoho Projects project.

## Endpoint

- **Method:** `GET`
- **Path:** `/portal/[:PORTALID]/projects/[:PROJECTID]/tasks`
- **Base URL:** `https://projectsapi.zoho.com/api/v3`
- **Official documentation:** [List Tasks By Project](https://projectsapi.zoho.com/api-docs#tasks_get-tasks-by-project)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PORTALID` | path | `string` | yes | Zoho Projects portal ID. |
| `PROJECTID` | path | `string` | yes | Zoho Projects project ID. |
| `sort_by` | query | `string` | no | Task sort expression. |
| `view_id` | query | `string` | no | Custom view ID. |
| `filter` | query | `string` | no | Raw JSON filter object from Zoho Projects. |
