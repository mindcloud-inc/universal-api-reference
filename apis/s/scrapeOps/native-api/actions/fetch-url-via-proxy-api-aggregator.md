# Fetch Url Via Proxy Api Aggregator with ScrapeOps

Fetches a URL through the ScrapeOps proxy aggregator.

## Endpoint

- **Method:** `GET`
- **Path:** `https://proxy.scrapeops.io/v1/`
- **Base URL:** `http://headers.scrapeops.io/v1`
- **Official documentation:** [Fetch Url Via Proxy Api Aggregator](https://scrapeops.io/docs/web-scraping-proxy-api-aggregator/quickstart/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | The URL to fetch through the ScrapeOps Proxy API Aggregator. |
| `render_js` | query | `boolean` | no | Enable JavaScript rendering for the target page. |
| `residential` | query | `boolean` | no | Use residential proxies for the request. |
| `country` | query | `string` | no | Two-letter country code for geotargeting. |
