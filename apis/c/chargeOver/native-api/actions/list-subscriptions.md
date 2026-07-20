# List Subscriptions with ChargeOver

Retrieves billing subscription records from ChargeOver.

## Endpoint

- **Method:** `GET`
- **Path:** `/package`
- **Base URL:** `https://{siteName}.chargeover.com/api/v3`
- **Official documentation:** [List Subscriptions](https://developer.chargeover.com/docs/api/querying-for-subscriptions/)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `expand` | query | `string` | no | Optional comma-separated related objects to expand in the subscription response. |
