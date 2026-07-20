# Search People By Job Title with ContactOut

Finds people in ContactOut by job title.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/people/search`
- **Base URL:** `https://api.contactout.com`
- **Official documentation:** [Search People By Job Title](https://api.contactout.com/#people-search-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_title` | body | `string` | no | Job title to search for. |
| `page` | body | `string` | no | Results page number. |
