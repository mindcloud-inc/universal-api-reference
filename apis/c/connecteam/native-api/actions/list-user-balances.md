# List User Balances with Connecteam

Retrieve a list of user time-off balances within a policy type

## Endpoint

- **Method:** `GET`
- **Path:** `/time-off/v1/policy-types/:policyTypeId/balances`
- **Base URL:** `https://api.connecteam.com`
- **Official documentation:** [List User Balances](https://developer.connecteam.com/reference/get_balances_time_off_v1_policy_types__policyTypeId__balances_get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `policyTypeId` | path | `string` | yes | — |
| `userIds` | query | `array<number>` | no | Send multiple values as a array. |
| `limit` | query | `number` | no | — |
| `offset` | query | `number` | no | — |
