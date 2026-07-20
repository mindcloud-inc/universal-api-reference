# List Workspace Sequences with Salesforge

Retrieves workspace sequences from Salesforge.

## Endpoint

- **Method:** `GET`
- **Path:** `/public/v2/workspaces/:workspaceID/sequences`
- **Base URL:** `https://api.salesforge.ai`
- **Official documentation:** [List Workspace Sequences](https://api.salesforge.ai/public/v2/docs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceID` | path | `string` | yes | Workspace ID to list sequences from. |
| `statuses` | query | `list<string>` | no | Only return sequences in the selected statuses. Send multiple values as a array. |
| `product_id` | query | `string` | no | Only return sequences for a specific product. |
| `sequence_ids` | query | `list<string>` | no | Only return the selected sequence IDs. Send multiple values as a array. |
| `type` | query | `string` | no | Only return sequences of the selected type. |
