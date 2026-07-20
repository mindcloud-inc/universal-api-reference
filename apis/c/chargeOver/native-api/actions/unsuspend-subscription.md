# Unsuspend Subscription with ChargeOver

Resumes a suspended subscription in ChargeOver.

## Endpoint

- **Method:** `POST`
- **Path:** `/package/:package_id/_action/unsuspend`
- **Base URL:** `https://{siteName}.chargeover.com/api/v3`
- **Official documentation:** [Unsuspend Subscription](https://developer.chargeover.com/docs/api/unsuspend-a-subscription/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `package_id` | path | `number` | yes | The ChargeOver subscription ID. |
