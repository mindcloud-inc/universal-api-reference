# List Project Issues with Zoho Projects

Retrieves issues from a Zoho Projects project.

## Endpoint

- **Method:** `GET`
- **Path:** `/portal/[:PORTALID]/projects/[:PROJECTID]/issues`
- **Base URL:** `https://projectsapi.zoho.com/api/v3`
- **Official documentation:** [List Project Issues](https://projectsapi.zoho.com/api-docs#issues_get-project-issues)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PORTALID` | path | `string` | yes | Zoho Projects portal ID. |
| `PROJECTID` | path | `string` | yes | Zoho Projects project ID. |
| `sort_by` | query | `string` | no | Issue sort expression. |
| `view_id` | query | `string` | no | Custom view ID. |
| `issue_ids` | query | `string` | no | Comma-separated issue IDs. |
| `filter` | query | `string` | no | Raw JSON filter object from Zoho Projects. |
