# List Prospects with Saleshandy

## Endpoint

- **Method:** `GET`
- **Path:** `/prospects`
- **Base URL:** `https://open-api.saleshandy.com/v1`
- **Official documentation:** [List Prospects](https://developer.saleshandy.com/)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Optional prospect search string. |
| `includeCustomFields` | query | `string` | no | Optional toggle to include custom field values. |
