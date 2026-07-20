# Create Subscription with Payrexx

Creates a subscription in Payrexx.

## Endpoint

- **Method:** `POST`
- **Path:** `Subscription/`
- **Base URL:** `https://api.payrexx.com/v1.14/`
- **Official documentation:** [Create Subscription](https://developers.payrexx.com/reference/create-a-new-subscription)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | body | `number` | yes | Webhook contact id for the subscription customer. |
| `psp` | body | `number` | yes | PSP id to use for the subscription. |
| `amount` | body | `number` | yes | Subscription amount in cents. |
| `currency` | body | `string` | yes | Subscription currency. |
| `purpose` | body | `string` | yes | Subscription payment purpose. |
| `paymentInterval` | body | `string` | yes | Subscription payment interval in PHP date interval format. |
| `period` | body | `string` | yes | Subscription period in PHP date interval format. |
| `cancellationInterval` | body | `string` | yes | Subscription cancellation interval in PHP date interval format. |
