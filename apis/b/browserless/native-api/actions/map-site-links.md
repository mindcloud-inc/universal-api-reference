# Map Site Links with Browserless

Retrieves discovered site links from Browserless.

## Endpoint

- **Method:** `POST`
- **Path:** `/map`
- **Base URL:** `https://production-sfo.browserless.io`
- **Official documentation:** [Map Site Links](https://docs.browserless.io/rest-apis/map)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | The base URL to crawl for links. |
| `search` | body | `string` | no | Optional query used to rank mapped links by relevance. |
| `limit` | body | `number` | no | Optional maximum number of links to return. |
| `sitemap` | body | `string` | no | Controls sitemap behavior. Valid values are `include`, `only`, and `skip`. |
| `includeSubdomains` | body | `boolean` | no | Whether to include URLs from subdomains. |
| `ignoreQueryParameters` | body | `boolean` | no | Whether to exclude URLs that include query parameters. |
