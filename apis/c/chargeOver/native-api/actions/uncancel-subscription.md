# Uncancel Subscription with ChargeOver

Reactivates a canceled subscription in ChargeOver.

## Endpoint

- **Method:** `POST`
- **Path:** `/package/:package_id/_action/uncancel`
- **Base URL:** `https://{siteName}.chargeover.com/api/v3`
- **Official documentation:** [Uncancel Subscription](https://developer.chargeover.com/docs/api/un-cancel-a-subscription/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `package_id` | path | `number` | yes | The ChargeOver subscription ID. |
