# Freeze Subscription with Peach

Updates a subscription payment in Peach by freezing it.

## Endpoint

- **Method:** `PUT`
- **Path:** `/payment/:paymentId`
- **Base URL:** `https://api.peach-in.com/v4`
- **Official documentation:** [Freeze Subscription](https://peach-organization.gitbook.io/peach/api-reference/payments/update-payment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `paymentId` | path | `string` | yes | The payment ID to update. |
| `freezeUntil` | body | `string` | yes | Freeze-until month in yyyy-mm format. |
