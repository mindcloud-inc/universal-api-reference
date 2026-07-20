# Crawl Web Pages with Langbase

## Endpoint

- **Method:** `POST`
- **Path:** `v1/tools/crawl`
- **Base URL:** `https://api.langbase.com`
- **Official documentation:** [Crawl Web Pages](https://langbase.com/docs/api-reference/tools/crawl)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `crawlKey` | body | `string` | yes | Langbase crawl key for the `LB-CRAWL-KEY` request header. |
| `url[]` | body | `array<string>` | yes | Array of URLs to crawl. |
| `service` | body | `list` | no | Crawler service to use. Accepted values: `0`, `1`. |
| `maxPages` | body | `number` | no | Maximum number of pages to crawl. |
