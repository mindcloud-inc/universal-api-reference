# List Subscribers with Kit

Lists subscribers in your Kit account.

## Endpoint

- **Method:** `GET`
- **Path:** `/subscribers`
- **Base URL:** `https://api.kit.com/v4`
- **Official documentation:** [List Subscribers](https://developers.kit.com/api-reference/subscribers/list-subscribers)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `after` | query | `string` | no | Pagination cursor to fetch subscribers after this position. |
| `before` | query | `string` | no | Pagination cursor to fetch subscribers before this position. |
| `page` | query | `number` | no | Page number for paginated subscriber results. |
| `per_page` | query | `number` | no | Number of subscribers to return per page. |
| `created_after` | query | `date` | no | Only include subscribers created after this timestamp. |
| `created_before` | query | `date` | no | Only include subscribers created before this timestamp. |
| `updated_after` | query | `date` | no | Only include subscribers updated after this timestamp. |
| `updated_before` | query | `date` | no | Only include subscribers updated before this timestamp. |
| `email_address` | query | `string` | no | Filter by an exact subscriber email address. |
| `status` | query | `list<string>` | no | Filter subscribers by lifecycle status. Accepted values: `active`, `bounced`, `cancelled`, `complained`, `inactive`. |
| `sort_field` | query | `list<string>` | no | Subscriber field used for sorting results. Accepted values: `created_at`, `email_address`, `first_name`, `last_name`, `state`. |
| `sort_order` | query | `list<string>` | no | Sort direction for subscriber results. Accepted values: `asc`, `desc`. |
| `include_total_count` | query | `boolean` | no | Whether to include total count metadata in the response. |
