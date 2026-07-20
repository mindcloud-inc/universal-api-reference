# List Badges with Navigatr

## Endpoint

- **Method:** `GET`
- **Path:** `/badge/`
- **Base URL:** `https://api.navigatr.app/v1`
- **Official documentation:** [List Badges](https://api.navigatr.app/docs#/Badge/badge_read_badges)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `issuer_id` | query | `number` | no | — |
| `community_id` | query | `number` | no | Community ID. Runtime verification shows this endpoint requires provider_id or community_id for this account. |
| `qa_community_id` | query | `number` | no | — |
| `provider_id` | query | `number` | no | Provider ID. Runtime verification shows this endpoint requires provider_id or community_id for this account. |
| `keyword` | query | `string` | no | — |
| `status` | query | `string` | no | — |
| `type` | query | `string` | no | — |
| `recipient_type` | query | `string` | no | — |
| `source` | query | `string` | no | — |
| `featured` | query | `boolean` | no | — |
| `qa_required` | query | `boolean` | no | — |
| `order_by` | query | `string` | no | — |
