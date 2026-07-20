# Search Web with Browserless

Retrieves web search results from Browserless.

## Endpoint

- **Method:** `POST`
- **Path:** `/search`
- **Base URL:** `https://production-sfo.browserless.io`
- **Official documentation:** [Search Web](https://docs.browserless.io/rest-apis/search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | The web search query to run. |
| `limit` | body | `number` | no | Optional maximum number of search results to return. |
| `categories[]` | body | `array<string>` | no | Optional category filters. Valid values are `github`, `pdf`, and `research`. |
| `sources[]` | body | `array<string>` | no | Optional source filters. Valid values are `images`, `news`, and `web`. |
| `tbs` | body | `string` | no | Optional time-based filter for the search results. |
