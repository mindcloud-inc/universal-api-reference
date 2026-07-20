# Get Sequence Analytics with Salesforge

Retrieves sequence analytics from Salesforge.

## Endpoint

- **Method:** `GET`
- **Path:** `/public/v2/workspaces/:workspaceID/sequences/:sequenceID/analytics`
- **Base URL:** `https://api.salesforge.ai`
- **Official documentation:** [Get Sequence Analytics](https://api.salesforge.ai/public/v2/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceID` | path | `string` | yes | Workspace ID for the sequence. |
| `sequenceID` | path | `string` | yes | Sequence ID to analyze. |
| `from_date` | query | `string` | yes | Start date for analytics in YYYY-MM-DD format. |
| `to_date` | query | `string` | yes | End date for analytics in YYYY-MM-DD format. |
| `timezone` | query | `string` | no | Optional timezone for analytics aggregation. |
