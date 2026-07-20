# Cancel Subscription with Cheddar

Cancels an existing customer subscription in Cheddar.

## Endpoint

- **Method:** `POST`
- **Path:** `/customers/cancel/productCode/{productCode}/code/:customerCode`
- **Base URL:** `https://getcheddar.com/xml`
- **Official documentation:** [Cancel Subscription](https://docs.getcheddar.com/#cancel-a-customer-39-s-subscription)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Customer code from Cheddar. |
