# List Comments with NeetoDesk

## Endpoint

- **Method:** `GET`
- **Path:** `/tickets/:ticket_id/comments`
- **Base URL:** `https://{workspaceSubdomain}.neetodesk.com/api/external/v2`
- **Official documentation:** [List Comments](https://apidocs.neetodesk.com/api-reference/comments/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ticket_id` | path | `string` | yes | Identifier of the ticket. |
