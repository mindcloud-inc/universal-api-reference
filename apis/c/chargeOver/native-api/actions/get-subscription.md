# Get Subscription with ChargeOver

Retrieves detailed subscription records from ChargeOver.

## Endpoint

- **Method:** `GET`
- **Path:** `/package/:package_id`
- **Base URL:** `https://{siteName}.chargeover.com/api/v3`
- **Official documentation:** [Get Subscription](https://developer.chargeover.com/docs/api/get-a-specific-subscription/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `expand` | query | `string` | no | Optional comma-separated related objects to expand in the subscription response. |
| `package_id` | path | `number` | yes | The ChargeOver subscription ID. |
