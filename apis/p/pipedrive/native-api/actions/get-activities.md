# Get Activities with Pipedrive

Retrieves activities from Pipedrive.

## Endpoint

- **Method:** `GET`
- **Path:** `v2/activities`
- **Base URL:** `{api_domain}/api`
- **Official documentation:** [Get Activities](https://developers.pipedrive.com/docs/api/v1/Activities#getActivities)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cursor` | query | `string` | no | Pagination cursor. |
| `filter_id` | query | `number` | no | Saved filter ID for activities. |
| `ids` | query | `string` | no | Comma-separated activity IDs. |
| `include_fields` | query | `string` | no | Comma-separated additional fields to include. |
| `lead_id` | query | `string` | no | Filter by lead ID. |
| `sort_by` | query | `string` | no | Sort field. |
| `sort_direction` | query | `string` | no | Sort direction, asc or desc. |
| `updated_since` | query | `string` | no | Return activities updated after this datetime. |
| `updated_until` | query | `string` | no | Return activities updated before this datetime. |
| `owner_id` | query | `number` | no | Owner user ID. |
| `deal_id` | query | `number` | no | Filter by deal ID. |
| `person_id` | query | `number` | no | Filter by person ID. |
| `org_id` | query | `number` | no | Filter by organization ID. |
| `done` | query | `boolean` | no | Filter by completion state. |
| `limit` | query | `number` | no | Max results per page. |
