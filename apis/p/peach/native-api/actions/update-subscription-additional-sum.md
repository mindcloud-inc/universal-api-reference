# Update Subscription Additional Sum with Peach

Updates a subscription payment in Peach with a new recurring sum.

## Endpoint

- **Method:** `PUT`
- **Path:** `/payment/:paymentId`
- **Base URL:** `https://api.peach-in.com/v4`
- **Official documentation:** [Update Subscription Additional Sum](https://peach-organization.gitbook.io/peach/api-reference/payments/update-payment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `paymentId` | path | `string` | yes | The payment ID to update. |
| `updatedSum` | body | `number` | yes | New recurring sum for the subscription. |
