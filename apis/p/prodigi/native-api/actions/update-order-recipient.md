# Update Order Recipient with Prodigi

Updates recipient details for a Prodigi order.

## Endpoint

- **Method:** `POST`
- **Path:** `/orders/[:prodigiOrderId]/actions/updateRecipient`
- **Base URL:** `https://api.prodigi.com/v4.0`
- **Official documentation:** [Update Order Recipient](https://www.prodigi.com/print-api/docs/reference/#update-recipient)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prodigiOrderId` | path | `string` | yes | Prodigi order ID to update. |
| `name` | body | `string` | yes | Updated recipient name. |
| `email` | body | `string` | yes | Updated recipient email address. |
| `phoneNumber` | body | `string` | yes | Updated recipient phone number. |
| `address` | body | `object` | yes | Updated recipient address object. |
