# List Prices with SureCart

## Endpoint

- **Method:** `GET`
- **Path:** `v1/prices`
- **Base URL:** `https://api.surecart.com`
- **Official documentation:** [List Prices](https://developer.surecart.com/api-reference/prices/list)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ad_hoc` | query | `boolean` | no | Only return prices that allow ad hoc amounts or not. |
| `archived` | query | `boolean` | no | Only return archived or active prices. |
