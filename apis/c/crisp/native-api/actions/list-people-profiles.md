# List People Profiles with Crisp

Retrieves people profiles from Crisp.

## Endpoint

- **Method:** `GET`
- **Path:** `/website/:website_id/people/profiles/:page_number`
- **Base URL:** `https://api.crisp.chat/v1`
- **Official documentation:** [List People Profiles](https://docs.crisp.chat/references/rest-api/v1/#list-people-profiles)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `website_id` | path | `string` | yes | The website identifier |
| `page_number` | path | `number` | no | Page number for people paging |
| `per_page` | query | `number` | no | Page size for people paging |
| `sort_field` | query | `string` | no | Sort on field |
| `sort_order` | query | `string` | no | Sort order |
| `search_operator` | query | `string` | no | Search operator |
| `search_filter` | query | `string` | no | Search filter |
| `search_text` | query | `string` | no | Search text |
| `filter_date_start` | query | `date` | no | When to start relative to profile creation date |
| `filter_date_end` | query | `date` | no | When to end relative to profile creation date |
