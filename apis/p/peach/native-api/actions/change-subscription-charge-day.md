# Change Subscription Charge Day with Peach

Updates a subscription payment in Peach with a new charge day.

## Endpoint

- **Method:** `PUT`
- **Path:** `/payment/:paymentId`
- **Base URL:** `https://api.peach-in.com/v4`
- **Official documentation:** [Change Subscription Charge Day](https://peach-organization.gitbook.io/peach/api-reference/payments/update-payment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `paymentId` | path | `string` | yes | The payment ID to update. |
| `updatedChargeDay` | body | `number` | yes | New day of month for charging, from 1 to 31. |
