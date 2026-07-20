# Get Paginated List of Tasks with Mihu AI

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/tasks`
- **Base URL:** `https://{subdomain}.mindhunters.ai`
- **Official documentation:** [Get Paginated List of Tasks](https://developers.mihu.ai/api-reference/tasks/get-paginated-list-of-tasks)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `agent_uuid` | query | `string` | no |
| `campaign_uuid` | query | `string` | no |
| `contact_uuid` | query | `string` | no |
| `page` | query | `number` | no |
| `per_page` | query | `number` | no |
| `priority` | query | `number` | no |
| `scheduled_from` | query | `string` | no |
| `scheduled_to` | query | `string` | no |
| `status` | query | `string` | no |
| `type` | query | `string` | no |
