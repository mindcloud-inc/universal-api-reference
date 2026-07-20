# List Actions with OnePageCRM

Retrieves actions from OnePageCRM.

## Endpoint

- **Method:** `GET`
- **Path:** `/actions`
- **Base URL:** `https://app.onepagecrm.com/api/v3`
- **Official documentation:** [List Actions](https://developer.onepagecrm.com/api/#/Actions/get_actions)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `done` | query | `boolean` | no | Only return completed actions. |
| `status` | query | `list<string>` | no | Return actions of a particular status. Accepted values: `asap`, `date`, `date_time`, `done`, `queued`, `queued_with_date`, `waiting`. |
| `assignee_id` | query | `string` | no | Return actions assigned to a specific user. |
| `contact_id` | query | `string` | no | Return actions for a specific contact. |
| `company_id` | query | `string` | no | Return actions for a specific company. |
| `date_filter` | query | `list<string>` | no | Choose which date field to use with Since or Until. Accepted values: `close_date`, `created_at`, `date`, `modified_at`, `updated_at`. |
| `since` | query | `date` | no | Return actions added or edited since this date or timestamp. |
| `until` | query | `date` | no | Return actions added or edited until this date or timestamp. |
| `modified_since` | query | `date` | no | Return only actions modified since this date or timestamp. |
| `unmodified_since` | query | `date` | no | Return only actions unmodified since this date or timestamp. |
