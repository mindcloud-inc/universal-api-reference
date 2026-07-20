# Search Companies with RocketReach

Finds companies in RocketReach.

## Endpoint

- **Method:** `POST`
- **Path:** `/searchCompany`
- **Base URL:** `https://api.rocketreach.co/api/v2`
- **Official documentation:** [Search Companies](https://docs.rocketreach.co/reference/company-search-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain[]` | body | `array<string>` | no | — |
| `name[]` | body | `array<string>` | no | — |
| `order_by` | body | `string` | no | Specifies the ordering of search results. Popularity matches the Search web app ordering. |
| `page_size` | body | `number` | no | Maximum number of results to return per page (1-100). |
| `query` | body | `object` | no | RocketReach CompanyQuery object. Pass any documented company-search filters here, including fields such as domain, name, industry, location, techstack, keyword, and other provider-supported nested keys. |
| `start` | body | `number` | no | Start index of the request results, counting from 1. |
