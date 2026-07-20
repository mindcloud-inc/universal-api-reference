# List Form Subscribers with Kit

Lists subscribers for a Kit form.

## Endpoint

- **Method:** `GET`
- **Path:** `/forms/:form_id/subscribers`
- **Base URL:** `https://api.kit.com/v4`
- **Official documentation:** [List Form Subscribers](https://developers.kit.com/api-reference/forms/list-subscribers-for-a-form)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_id` | path | `number` | yes | The ID of the form. |
| `status` | query | `list` | no | Filter subscribers by status. Accepted values: `active`, `all`, `bounced`, `cancelled`, `complained`, `inactive`. |
| `email_address` | query | `string` | no | Filter by exact email address. |
| `added_after` | query | `date` | no | Filter subscribers added after this timestamp. |
| `added_before` | query | `date` | no | Filter subscribers added before this timestamp. |
| `created_after` | query | `date` | no | Filter subscribers created after this timestamp. |
| `created_before` | query | `date` | no | Filter subscribers created before this timestamp. |
| `after` | query | `string` | no | Return results after this cursor. |
| `before` | query | `string` | no | Return results before this cursor. |
| `include_total_count` | query | `boolean` | no | Include total_count in pagination metadata. |
| `per_page` | query | `number` | no | Number of results per page. |
| `sort_order` | query | `list` | no | Sort order for results. Accepted values: `asc`, `desc`. |
