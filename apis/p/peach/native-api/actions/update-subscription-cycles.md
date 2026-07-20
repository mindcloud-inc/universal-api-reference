# Update Subscription Cycles with Peach

Updates a subscription payment in Peach with new billing cycles.

## Endpoint

- **Method:** `PUT`
- **Path:** `/payment/:paymentId`
- **Base URL:** `https://api.peach-in.com/v4`
- **Official documentation:** [Update Subscription Cycles](https://peach-organization.gitbook.io/peach/api-reference/payments/update-payment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `paymentId` | path | `string` | yes | The payment ID to update. |
| `updatedCycles` | body | `number` | yes | New number of billing cycles. Use 999 for unlimited. |
