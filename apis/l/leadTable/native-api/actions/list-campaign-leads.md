# List campaign leads with LeadTable

## Endpoint

- **Method:** `GET`
- **Path:** `/lead/campaign/{campaignID}`
- **Base URL:** `https://api.lead-table.com/api/v3/external`
- **Official documentation:** [List campaign leads](https://docs.lead-table.com/leadtable-external-api-v3)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignID` | path | `string` | yes | The campaign or table whose leads should be listed. |
