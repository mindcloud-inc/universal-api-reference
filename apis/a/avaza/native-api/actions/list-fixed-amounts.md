# List Fixed Amounts with Avaza

Retrieves fixed-amount entries from Avaza.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/FixedAmount`
- **Base URL:** `https://api.avaza.com`
- **Official documentation:** [List Fixed Amounts](https://api.avaza.com/#!/FixedAmount/FixedAmount_Get)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `UpdatedAfter` | query | `date` | no | — |
| `ProjectID` | query | `number` | no | (Optional) The ProjectID of a Project to filter Fixed Amounts for |
| `TaskID` | query | `number` | no | (Optional) The TaskID of a Task to filter Fixed Amounts for |
| `isInvoiced` | query | `boolean` | no | — |
