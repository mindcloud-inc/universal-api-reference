# List Workspace Members with Lumin

## Endpoint

- **Method:** `GET`
- **Path:** `/workspaces/members`
- **Base URL:** `https://api.luminpdf.com/v1`
- **Official documentation:** [List Workspace Members](https://developers.luminpdf.com/api/get-workspace-members/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Which page of members to return. |
| `limit` | query | `number` | no | How many members to return. One of 10, 25, or 50. |
