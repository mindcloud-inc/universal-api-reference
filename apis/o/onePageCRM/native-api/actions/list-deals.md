# List Deals with OnePageCRM

Retrieves deals from OnePageCRM.

## Endpoint

- **Method:** `GET`
- **Path:** `/deals`
- **Base URL:** `https://app.onepagecrm.com/api/v3`
- **Official documentation:** [List Deals](https://developer.onepagecrm.com/api/#/Deals/get_deals)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | Search deals by name |
| `search` | query | `string` | no | Search deals by deal name, contact name, or company name |
| `status` | query | `list<string>` | no | Return deals of a particular status Accepted values: `closed`, `lost`, `pending`, `won`. |
| `pipeline_id` | query | `list<string>` | no | Return deals from the specified pipeline |
| `sales_pipeline_id` | query | `list<string>` | no | Return deals referencing the specified sales pipeline |
| `owner_id` | query | `list<string>` | no | Return deals owned by a specific user |
| `company_id` | query | `list<string>` | no | Return deals for a specific company |
| `contact_id` | query | `list<string>` | no | Return deals for a specific contact |
| `tag` | query | `string` | no | Filter deals by tag |
| `filter_id` | query | `string` | no | Apply a saved filter to the deal listing |
| `stage` | query | `number` | no | Return pending deals with the specified deal stage |
| `date_filter` | query | `list<string>` | no | Choose which date field to use with date-range filtering Accepted values: `close_date`, `created_at`, `date`, `expected_close_date`, `modified_at`, `updated_at`. |
| `since` | query | `date` | no | Start of the date range filter |
| `until` | query | `date` | no | End of the date range filter |
| `modified_since` | query | `date` | no | Return only resources that were modified since the specified time |
| `unmodified_since` | query | `date` | no | Return only resources that were unmodified since the specified time |
| `include_history` | query | `boolean` | no | Include deal stage history in the response |
