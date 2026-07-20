# Update Payment Field with Peach

Updates a payment field in Peach.

## Endpoint

- **Method:** `PUT`
- **Path:** `/payment/:paymentId`
- **Base URL:** `https://api.peach-in.com/v4`
- **Official documentation:** [Update Payment Field](https://peach-organization.gitbook.io/peach/api-reference/payments/update-payment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `paymentId` | path | `string` | yes | The payment ID to update. |
| `key` | body | `string` | yes | The payment field key to update, for example donorFirstName. |
| `value` | body | `string` | yes | The new value for the selected field. |
