# Search People With Contact Reveal with ContactOut

Finds people in ContactOut with revealed contact information.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/people/search`
- **Base URL:** `https://api.contactout.com`
- **Official documentation:** [Search People With Contact Reveal](https://api.contactout.com/#people-search-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company` | body | `string` | no | Filter by current or past company. |
| `job_title` | body | `string` | no | Filter by job title. |
| `name` | body | `string` | no | Match people by name. |
| `page` | body | `string` | no | Results page number. |
