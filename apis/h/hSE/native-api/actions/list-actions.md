# List Actions with 4HSE

Retrieves actions from 4HSE.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/action/index`
- **Base URL:** `https://service.4hse.com`
- **Official documentation:** [List Actions](https://docs.4hse.com/en/api/action/#operation-indexAction-post)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | body | `object` | no | Action filters. |
| `filter.action_id` | body | `string` | no | Find one action by id. |
| `filter.action_type` | body | `string` | no | Filter by preventive action type. Accepted values: `0`, `1`, `2`, `3`, `4`. |
| `filter.name` | body | `string` | no | Search an action by name. |
| `filter.subtenant_id` | body | `string` | no | Filter by office id. |
| `filter.tenant_id` | body | `string` | no | Filter by project id. |
| `history` | body | `boolean` | no | Include historicized entries when true. |
