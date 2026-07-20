# Create Webset Search with Exa

Creates a new webset search in Exa.

## Endpoint

- **Method:** `POST`
- **Path:** `/websets/v0/websets/:webset/searches`
- **Base URL:** `https://api.exa.ai`
- **Official documentation:** [Create Webset Search](https://exa.ai/docs/websets/api/websets/searches/create-a-search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webset` | path | `string` | yes | The id of the Webset |
| `count` | body | `number` | yes | Number of Items the Search will attempt to find.  The actual number of Items found may be less than this number depending on the query complexity. |
| `query` | body | `string` | yes | Natural language search query describing what you are looking for.  Be specific and descriptive about your requirements, characteristics, and any constraints that help narrow down the results.  Any URLs provided will be crawled and used as additional context for the search. |
| `entity.type` | body | `string` | no | — |
| `entity.description` | body | `string` | no | — |
| `criteria` | body | `string` | no | Criteria every item is evaluated against.  It's not required to provide your own criteria, we automatically detect the criteria from all the information provided in the query. Only use this when you need more fine control. |
| `exclude` | body | `string` | no | Sources (existing imports or websets) to exclude from search results. Any results found within these sources will be omitted to prevent finding them during search. |
| `scope` | body | `string` | no | Limit the search to specific sources (existing imports). Any results found within these sources matching the search criteria will be included in the Webset. |
| `recall` | body | `string` | no | Whether to provide an estimate of how many total relevant results could exist for this search. Result of the analysis will be available in the `recall` field within the search request. |
| `behavior` | body | `string` | no | — |
| `metadata` | body | `string` | no | Set of key-value pairs you want to associate with this object. |
