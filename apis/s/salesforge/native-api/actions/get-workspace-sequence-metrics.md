# Get Workspace Sequence Metrics with Salesforge

Retrieves workspace sequence metrics from Salesforge.

## Endpoint

- **Method:** `GET`
- **Path:** `/public/v2/workspaces/:workspaceID/sequence-metrics`
- **Base URL:** `https://api.salesforge.ai`
- **Official documentation:** [Get Workspace Sequence Metrics](https://api.salesforge.ai/public/v2/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceID` | path | `string` | yes | Workspace ID for the metrics query. |
| `product_id` | query | `string` | no | Only include metrics for a specific product. |
| `sequence_ids` | query | `list<string>` | no | Only include metrics for the selected sequences. Send multiple values as a array. |
