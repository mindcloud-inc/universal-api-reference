# List Invoices with Centerpoint

## Endpoint

- **Method:** `GET`
- **Path:** `invoices`
- **Base URL:** `https://api.centerpointconnect.io/centerpoint/`
- **Official documentation:** [List Invoices](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/invoicesGET)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter[lastSentAt]` | query | `string` | no | Start of the “Last Sent At” date range (inclusive). |
| `filter[lastSentAt][lt]` | query | `string` | no | End of the “Last Sent At” date range (exclusive / less-than). |
| `fields[productions]` | query | `string` | no | Optional fields productions query parameter. |
| `filter[lastSentAt][timezone]` | query | `string` | no | — |
| `fields[properties]` | query | `string` | no | Optional fields properties query parameter. |
| `include` | query | `string` | no | — |
| `fields[companies]` | query | `string` | no | Optional fields companies query parameter. |
| `fields[employees]` | query | `string` | no | Optional fields employees query parameter. |
| `fields[profiles]` | query | `string` | no | Optional fields profiles query parameter. |
| `aggregates[subtotal][0]` | query | `string` | no | Optional aggregates subtotal  0 query parameter. |
| `aggregates[amount][0]` | query | `string` | no | Optional aggregates amount  0 query parameter. |
| `aggregates[margin][0]` | query | `string` | no | Optional aggregates margin  0 query parameter. |
| `aggregates[cost][0]` | query | `string` | no | Optional aggregates cost  0 query parameter. |
