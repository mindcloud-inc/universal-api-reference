# Update Order Shipping Method with Prodigi

Updates the shipping method for a Prodigi order.

## Endpoint

- **Method:** `POST`
- **Path:** `/orders/[:prodigiOrderId]/actions/updateShippingMethod`
- **Base URL:** `https://api.prodigi.com/v4.0`
- **Official documentation:** [Update Order Shipping Method](https://www.prodigi.com/print-api/docs/reference/#update-shipping-method)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prodigiOrderId` | path | `string` | yes | Prodigi order ID to update. |
| `shippingMethod` | body | `string` | yes | New shipping method: budget, standard, standardplus, express, overnight. |
