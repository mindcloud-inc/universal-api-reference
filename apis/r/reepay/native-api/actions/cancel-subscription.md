# Cancel Subscription with Reepay

Cancels a subscription in Reepay.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/subscription/:handle/cancel`
- **Base URL:** `https://api.frisbii.com`
- **Official documentation:** [Cancel Subscription](https://docs.frisbii.com/reference/cancelsubscription)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `handle` | path | `string` | yes | Subscription handle from Reepay. |
