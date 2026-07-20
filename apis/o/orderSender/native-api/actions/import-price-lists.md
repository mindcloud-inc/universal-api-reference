# Import Price Lists with Order Sender

Imports price lists into Order Sender.

## Endpoint

- **Method:** `POST`
- **Path:** `/op/import/res/listini`
- **Base URL:** `https://business.ordersender.com/api/v1`
- **Official documentation:** [Import Price Lists](https://developer.ordersender.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fornitore` | query | `string` | no | Supplier code required when importing price lists. |
| `records` | body | `string` | no | Array of price list records to import. |
