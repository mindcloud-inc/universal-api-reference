# Get Organic Search Results with DataForSEO

Retrieves organic search results from DataForSEO.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/serp/:search_engine/organic/live/advanced.ai`
- **Base URL:** `https://api.dataforseo.com`
- **Official documentation:** [Get Organic Search Results](https://docs.dataforseo.com/v3/serp-se-type-live-advanced/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search_engine` | path | `list<string>` | yes | Search engine name. Accepted values: `bing`, `google`, `yahoo`. |
| `keyword` | body | `string` | yes | Search keyword. |
| `language_code` | body | `string` | yes | Search engine language code. |
| `location_name` | body | `string` | yes | Full location name in hierarchical comma-separated format. |
| `device` | body | `list<string>` | no | Device type. Accepted values: `desktop`, `mobile`. |
| `depth` | body | `number` | no | Number of results in the SERP. |
| `max_crawl_pages` | body | `number` | no | Number of search results pages to crawl. |
| `people_also_ask_click_depth` | body | `number` | no | Click depth on the people_also_ask element. |
