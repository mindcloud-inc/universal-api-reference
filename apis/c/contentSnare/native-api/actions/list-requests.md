# List Requests with Content Snare

Retrieves requests from Content Snare.

## Endpoint

- **Method:** `GET`
- **Path:** `/partner_api/v1/requests`
- **Base URL:** `https://api.contentsnare.com`
- **Official documentation:** [List Requests](https://api.contentsnare.com/partner_api/v1/documentation)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | String to search in the values specified in the parameter `q_by[]` |
| `q_by[]` | query | `array<string>` | no | Specifies list of values where string from the parameter `q` will be searched. If it isn't set then the default list is used.<br><b>Examples:</b> q_by[]=name&q_by[]=clients.full_name&q_by[]=client_companies.name |
| `filter_by[statuses]` | query | `object` | no | Filter By. |
| `filter_by[statuses][]` | query | `array<string>` | no | Specifies list of statuses for filtering<br><b>Examples:</b> filter_by[statuses][]=published&filter_by[statuses][]=completed |
| `sort_by` | query | `string` | no | Specifies value for sorting |
| `sort_direction` | query | `string` | no | Specifies direction for sorting |
| `expand[]` | query | `array<string>` | no | Include additional data in response<br><b>Examples:</b> expand[]=request_template_name&expand[]=owner_email&expand[]=owner_name&expand[]=clients |
