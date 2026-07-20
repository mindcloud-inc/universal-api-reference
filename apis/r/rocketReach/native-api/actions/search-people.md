# Search People with RocketReach

Finds people in RocketReach.

## Endpoint

- **Method:** `POST`
- **Path:** `/person/search`
- **Base URL:** `https://api.rocketreach.co/api/v2`
- **Official documentation:** [Search People](https://docs.rocketreach.co/reference/people-search-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `current_employer[]` | body | `array<string>` | no | — |
| `name[]` | body | `array<string>` | no | — |
| `order_by` | body | `string` | no | Specifies the ordering of search results. Popularity matches the Search web app ordering. |
| `page_size` | body | `number` | no | Maximum number of results to return per page (1-100). |
| `query` | body | `object` | no | RocketReach PersonQuery object. Pass any documented people-search filters here, including fields such as name, current_employer, current_title, department, geo, skills, company filters, and other provider-supported nested keys. |
| `start` | body | `number` | no | Start index of the request results, counting from 1. |
