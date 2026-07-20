# List Placement Tests with SuperSend

Retrieves placement tests from SuperSend.

## Endpoint

- **Method:** `GET`
- **Path:** `/placement-tests`
- **Base URL:** `https://api.supersend.io/v2`
- **Official documentation:** [List Placement Tests](https://docs.supersend.io/docs/placement-test)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team_id` | query | `string` | no | — |
| `sender_id` | query | `string` | no | — |
| `status` | query | `string` | no | Allowed values: pending, sending, sent, completed, failed. |
| `search` | query | `string` | no | — |
| `conditional_filters` | query | `string` | no | JSON string for score/date filters |
| `sort_by` | query | `string` | no | Allowed values: created_at, name, status, score, sent_at, completed_at. Default: created_at. |
| `sort_order` | query | `string` | no | Allowed values: asc, desc. Default: desc. |
| `limit` | query | `number` | no | Default: 50. Range: 1 to 100. |
| `offset` | query | `number` | no | Default: 0. Range: 0 to inf. |
