# Import Products with Order Sender

Imports product records into Order Sender.

## Endpoint

- **Method:** `POST`
- **Path:** `/op/import/res/prodotti`
- **Base URL:** `https://business.ordersender.com/api/v1`
- **Official documentation:** [Import Products](https://developer.ordersender.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fornitore` | query | `string` | no | Optional supplier code for product import. |
| `records` | body | `string` | no | Array of product records to import. |
