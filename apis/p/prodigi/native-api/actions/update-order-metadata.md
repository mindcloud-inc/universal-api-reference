# Update Order Metadata with Prodigi

Updates metadata for a Prodigi order.

## Endpoint

- **Method:** `POST`
- **Path:** `/orders/[:prodigiOrderId]/actions/updateMetadata`
- **Base URL:** `https://api.prodigi.com/v4.0`
- **Official documentation:** [Update Order Metadata](https://www.prodigi.com/print-api/docs/reference/#update-metadata)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prodigiOrderId` | path | `string` | yes | Prodigi order ID to update. |
| `metadata` | body | `object` | yes | Replacement metadata object for the order. |
