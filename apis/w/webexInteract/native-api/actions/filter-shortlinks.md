# Filter shortlinks with Webex Interact

Finds shortlinks in Webex Interact by filter criteria.

## Endpoint

- **Method:** `POST`
- **Path:** `/assets/v1/shortlink/filter`
- **Base URL:** `https://api.webexinteract.com`
- **Official documentation:** [Filter shortlinks](https://docs.webexinteract.com/reference/shortlinks-api)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter.created_at_end` | body | `date` | no | Filter shortlinks created before this ISO 8601 timestamp. |
| `filter.created_at_start` | body | `date` | no | Filter shortlinks created after this ISO 8601 timestamp. |
| `filter.query` | body | `string` | no | Fuzzy search text for shortlink title or tags. |
| `page.page_number` | body | `string` | no | Page number to return. |
| `page.page_size` | body | `string` | no | Number of shortlinks per page. |
| `sort.sort_order` | body | `string` | no | Sort order: ASC or DESC. |
| `filter.tags` | body | `list<string>` | no | Exact-match tag filters. |
