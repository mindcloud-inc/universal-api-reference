# Create async scraping job with Scrape do

Creates a new async scraping job in Scrape do.

## Endpoint

- **Method:** `POST`
- **Path:** `https://q.scrape.do/api/v1/jobs`
- **Base URL:** `https://api.scrape.do`
- **Official documentation:** [Create async scraping job](https://scrape.do/documentation/async-api/create-job/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `GeoCode` | body | `string` | no | Country code for geo-targeting async jobs. |
| `Method` | body | `string` | no | HTTP method to use for each target request. |
| `Targets[]` | body | `array<string>` | yes | One or more URLs to scrape asynchronously. Send multiple values as a array. |
