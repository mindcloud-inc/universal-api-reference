# List Subscriptions with Recurly

## Endpoint

- **Method:** `GET`
- **Path:** `/subscriptions`
- **Base URL:** `https://v3.recurly.com`
- **Official documentation:** [List Subscriptions](https://recurly.com/developers/api/v2021-02-25/#operation/list_subscriptions)

## Capabilities

This operation supports [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `begin_time` | query | `string` | no | — |
| `end_time` | query | `string` | no | — |
| `ids` | query | `string` | no | — |
| `state` | query | `string` | no | Accepted values: `0`, `1`, `2`, `3`, `4`, `5`. |
