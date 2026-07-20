# Search People By Company with ContactOut

Finds people in ContactOut by company.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/people/search`
- **Base URL:** `https://api.contactout.com`
- **Official documentation:** [Search People By Company](https://api.contactout.com/#people-search-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company` | body | `string` | no | Company name to search people within. |
| `page` | body | `string` | no | Results page number. |
