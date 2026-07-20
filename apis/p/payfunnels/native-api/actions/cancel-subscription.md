# Cancel Subscription with Payfunnels

Updates a subscription by cancelling it in Payfunnels.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/subscriptions/cancel`
- **Base URL:** `https://api.payfunnels.com`
- **Official documentation:** [Cancel Subscription](https://api.payfunnels.com/api/docs/#cancel-subscription)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cancelDate` | body | `number` | no | Unix timestamp used when cancellation option is custom_date. |
| `cancellationOption` | body | `string` | yes | When to cancel the subscription. |
| `id` | body | `string` | yes | ID of the subscription to cancel. |
