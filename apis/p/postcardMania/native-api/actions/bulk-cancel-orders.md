# Bulk Cancel Orders with PostcardMania

Cancels existing orders in PostcardMania in bulk.

## Endpoint

- **Method:** `POST`
- **Path:** `/order/bulk-cancel`
- **Base URL:** `https://v3.pcmintegrations.com`
- **Official documentation:** [Bulk Cancel Orders](https://docs.pcmintegrations.com/docs/directmail-api/gan0r8uot3zqe)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orders` | body | `list<number>` | yes | Array of PostcardMania order IDs to cancel in bulk. |
