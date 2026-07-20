# Update Contract with Oneflow

Updates an existing contract in Oneflow.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contracts/:id`
- **Base URL:** `https://api.oneflow.com/v1`
- **Official documentation:** [Update Contract](https://developer.oneflow.com/reference/update-a-contract-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Oneflow contract ID. |
| `_private.name` | body | `string` | no | Update the contract name. |
| `_private.value.amount` | body | `string` | no | Update the contract value amount. |
| `_private.signing_period_expiration.type` | body | `string` | no | Set the signing period expiration type. |
| `_private.signing_period_expiration.expire_days_after_publish` | body | `number` | no | Set the number of signing days after publish when using days_after_publish. |
