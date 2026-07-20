# Search Companies HQ Only with ContactOut

Finds HQ-only companies in ContactOut using company search filters.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/company/search`
- **Base URL:** `https://api.contactout.com`
- **Official documentation:** [Search Companies HQ Only](https://api.contactout.com/#company-search-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | body | `string` | no | Company domain to search. |
| `name` | body | `string` | no | Company name to search. |
| `page` | body | `string` | no | Results page number. |
