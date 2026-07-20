# List customer campaigns with LeadTable

## Endpoint

- **Method:** `GET`
- **Path:** `/campaign/all/{customerID}`
- **Base URL:** `https://api.lead-table.com/api/v3/external`
- **Official documentation:** [List customer campaigns](https://docs.lead-table.com/leadtable-external-api-v3)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerID` | path | `string` | yes | The customer whose campaigns should be listed. |
