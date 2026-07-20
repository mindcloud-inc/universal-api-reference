# Start Crawl with Kadoa

## Endpoint

- **Method:** `POST`
- **Path:** `/v4/crawl/`
- **Base URL:** `https://api.kadoa.com`
- **Official documentation:** [Start Crawl](https://docs.kadoa.com/api-reference/crawling/start-crawling-session)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | URL to crawl |
| `maxPages` | body | `number` | no | Maximum pages to crawl |
| `maxDepth` | body | `number` | no | Maximum crawl depth |
| `strictDomain` | body | `boolean` | no | Only crawl within same domain |
| `proxyType` | body | `string` | no | Proxy type to use |
| `proxyCountry` | body | `string` | no | Proxy country ISO code |
| `timeout` | body | `number` | no | Timeout in milliseconds |
| `callbackUrl` | body | `string` | no | Webhook URL for completion callback |
