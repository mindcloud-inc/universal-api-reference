# Suspend Subscription with ChargeOver

Suspends an existing subscription in ChargeOver.

## Endpoint

- **Method:** `POST`
- **Path:** `/package/:package_id/_action/suspend`
- **Base URL:** `https://{siteName}.chargeover.com/api/v3`
- **Official documentation:** [Suspend Subscription](https://developer.chargeover.com/docs/api/suspend-a-subscription/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `package_id` | path | `number` | yes | The ChargeOver subscription ID. |
