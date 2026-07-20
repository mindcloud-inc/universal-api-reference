# Delete Payment Method with LimoExpress

Deletes an existing payment method from LimoExpress.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/integration/payment-methods`
- **Base URL:** `https://api.limoexpress.me`
- **Official documentation:** [Delete Payment Method](https://api.limoexpress.me/api/docs/v1#/Payment%20Methods/deleteAOrganisationPaymentMethod)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | Identifier of the payment method to delete. |
