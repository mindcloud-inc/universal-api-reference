# Cancel Subscription with ChargeOver

Cancels an existing subscription in ChargeOver.

## Endpoint

- **Method:** `POST`
- **Path:** `/package/:package_id/_action/cancel`
- **Base URL:** `https://{siteName}.chargeover.com/api/v3`
- **Official documentation:** [Cancel Subscription](https://developer.chargeover.com/docs/api/cancel-a-subscription/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `package_id` | path | `number` | yes | The ChargeOver subscription ID. |
