# List Action Subscriptions with 4HSE

Retrieves action subscriptions from 4HSE.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/action-subscription/index`
- **Base URL:** `https://service.4hse.com`
- **Official documentation:** [List Action Subscriptions](https://docs.4hse.com/en/api/actionsubscription/#operation-indexActionSubscription-post)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter.action_subscription_id` | body | `string` | no | Filter by compliance schedule entry ID. |
| `filter.action_id` | body | `string` | no | Filter by preventive action. |
| `filter.action_type` | body | `string` | no | Filter by action type. Accepted values: `0`, `1`, `2`, `3`, `4`. |
| `filter.subscriber_id` | body | `string` | no | Filter by subscribed resource. |
| `filter.subscriber_type` | body | `string` | no | Filter by subscribed resource type. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`. |
| `filter.status` | body | `string` | no | Filter by compliance status. Accepted values: `0`, `1`, `2`, `3`. |
| `filter.subtenant_id` | body | `string` | no | Filter by office. |
| `filter.tenant_id` | body | `string` | no | Filter by project. |
| `history` | body | `boolean` | no | Include historicized entries in the results. |
