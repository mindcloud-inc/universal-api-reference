# List Tickets with NeetoDesk

## Endpoint

- **Method:** `GET`
- **Path:** `/tickets`
- **Base URL:** `https://{workspaceSubdomain}.neetodesk.com/api/external/v2`
- **Official documentation:** [List Tickets](https://apidocs.neetodesk.com/api-reference/tickets/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `string` | no | Filter tickets by status. |
