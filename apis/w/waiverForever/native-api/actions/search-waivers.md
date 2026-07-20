# Search Waivers with WaiverForever

Finds waivers in WaiverForever by search criteria.

## Endpoint

- **Method:** `POST`
- **Path:** `/openapi/v1/waiver/search`
- **Base URL:** `https://api.waiverforever.com`
- **Official documentation:** [Search Waivers](https://docs.waiverforever.com/#waiver-search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end_timestamp` | body | `number` | no | End timestamp in seconds. |
| `page` | body | `number` | no | Results page number. |
| `per_page` | body | `number` | no | Results returned per page. |
| `search_term` | body | `string` | no | Search keyword. |
| `start_timestamp` | body | `number` | no | Start timestamp in seconds. |
| `template_ids` | body | `list<string>` | no | Template ids to constrain the search. Send multiple values as a array. |
