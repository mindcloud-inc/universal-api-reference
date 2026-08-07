# List Return Orders with ShipBob

## Endpoint

- **Method:** `GET`
- **Path:** `2026-07/return`
- **Base URL:** `https://{apiSubdomain}.shipbob.com/`
- **API:** REST - Cursor
- **Official documentation:** [List Return Orders](https://developer.shipbob.com/api/returns/get-return-orders)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Ids` | query | `string` | no | Comma-separated return order IDs. Send multiple values as a string separated by `,`. |
| `ReferenceIds` | query | `string` | no | Comma-separated return reference IDs or RMA numbers. Send multiple values as a string separated by `,`. |
| `Status` | query | `list<string>` | no | One or more return statuses: AwaitingArrival, Arrived, Processing, Completed, or Cancelled. Accepted values: `Arrived`, `AwaitingArrival`, `Cancelled`, `Completed`, `Processing`. Send multiple values as a string separated by `,`. |
| `FulfillmentCenterIds` | query | `list<number>` | no | Comma-separated fulfillment center IDs. Send multiple values as a string separated by `,`. |
| `TrackingNumbers` | query | `string` | no | Comma-separated return tracking numbers. Send multiple values as a string separated by `,`. |
| `OriginalShipmentIds` | query | `string` | no | Comma-separated original shipment IDs. Send multiple values as a string separated by `,`. |
| `InventoryIds` | query | `list<number>` | no | Comma-separated inventory IDs. Send multiple values as a string separated by `,`. |
| `StartDate` | query | `date` | no | Return orders created on or after this ISO 8601 date and time. |
| `EndDate` | query | `date` | no | Return orders created on or before this ISO 8601 date and time. |
| `ReturnTypes` | query | `list<string>` | no | Comma-separated return types, such as Regular or ReturnToSender. Accepted values: `Regular`, `ReturnToSender`. Send multiple values as a string separated by `,`. |
| `ReturnActions` | query | `list<string>` | no | Comma-separated requested actions, such as Restock, Quarantine, or Dispose. Accepted values: `Default`, `Dispose`, `Quarantine`, `Restock`. Send multiple values as a string separated by `,`. |
| `StoreOrderIds` | query | `string` | no | Comma-separated store order IDs. Send multiple values as a string separated by `,`. |
| `CompletedStartDate` | query | `date` | no | Return orders completed on or after this ISO 8601 date and time. |
| `CompletedEndDate` | query | `date` | no | Return orders completed on or before this ISO 8601 date and time. |
