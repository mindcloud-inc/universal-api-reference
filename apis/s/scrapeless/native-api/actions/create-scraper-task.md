# Create Scraper Task with Scrapeless

Creates a new scraper task in Scrapeless.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/scraper/request`
- **Base URL:** `https://api.scrapeless.com`
- **Official documentation:** [Create Scraper Task](https://apidocs.scrapeless.com/api-11949852)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `actor` | body | `string` | yes | — |
| `input` | body | `object` | yes | — |
| `input.url` | body | `string` | yes | — |
| `proxy` | body | `object` | yes | — |
| `proxy.country` | body | `string` | yes | — |
| `async` | body | `boolean` | no | If true, the task will be executed asynchronously.  If false, the task will be executed synchronously. |
