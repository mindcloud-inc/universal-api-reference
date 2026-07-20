# Get Sequence Contact Sending Data with Salesforge

Retrieves sequence contact sending data from Salesforge.

## Endpoint

- **Method:** `GET`
- **Path:** `/public/v2/workspaces/:workspaceID/sending-data`
- **Base URL:** `https://api.salesforge.ai`
- **Official documentation:** [Get Sequence Contact Sending Data](https://api.salesforge.ai/public/v2/docs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceID` | path | `string` | yes | Workspace ID for the sending data query. |
| `sequence_ids` | query | `list<string>` | no | Only include sending data for the selected sequences. Send multiple values as a array. |
