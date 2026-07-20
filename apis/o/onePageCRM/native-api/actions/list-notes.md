# List Notes with OnePageCRM

Retrieves notes from OnePageCRM.

## Endpoint

- **Method:** `GET`
- **Path:** `/notes`
- **Base URL:** `https://app.onepagecrm.com/api/v3`
- **Official documentation:** [List Notes](https://developer.onepagecrm.com/api/#/Notes/get_notes)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | query | `string` | no | Return notes for a specific contact. |
| `company_id` | query | `string` | no | Return notes for a specific company. |
| `date_filter` | query | `list<string>` | no | Choose which date field to use with Since or Until. Accepted values: `created_at`, `date`, `modified_at`, `updated_at`. |
| `since` | query | `date` | no | Return notes added or edited since this date or timestamp. |
| `until` | query | `date` | no | Return notes added or edited until this date or timestamp. |
| `modified_since` | query | `date` | no | Return only notes modified since this date or timestamp. |
| `unmodified_since` | query | `date` | no | Return only notes unmodified since this date or timestamp. |
