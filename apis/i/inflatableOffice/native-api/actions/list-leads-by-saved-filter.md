# List Leads By Saved Filter with InflatableOffice

Retrieves leads by saved filter from InflatableOffice.

## Endpoint

- **Method:** `GET`
- **Path:** `/leads`
- **Base URL:** `https://rental.software/api6`
- **Official documentation:** [List Leads By Saved Filter](https://rental.software/support/knowledge-base/article/api-leads-list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `string` | yes | Name of a saved InflatableOffice lead filter to apply before listing leads. |
