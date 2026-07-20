# List Team Members with NeetoDesk

## Endpoint

- **Method:** `GET`
- **Path:** `/team-members`
- **Base URL:** `https://{workspaceSubdomain}.neetodesk.com/api/external/v2`
- **Official documentation:** [List Team Members](https://apidocs.neetodesk.com/api-reference/team-members/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | no | Filter team members by email address. |
