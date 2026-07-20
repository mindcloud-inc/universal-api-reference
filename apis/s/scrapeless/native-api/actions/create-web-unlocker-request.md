# Create Web Unlocker Request with Scrapeless

Creates a web unlocker request in Scrapeless.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/unlocker/request`
- **Base URL:** `https://api.scrapeless.com`
- **Official documentation:** [Create Web Unlocker Request](https://apidocs.scrapeless.com/api-11949854)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input` | body | `object` | yes | — |
| `input.url` | body | `string` | yes | request url |
| `input.redirect` | body | `boolean` | no | whether redirect request |
| `input.method` | body | `string` | yes | request method |
| `input.header` | body | `object` | no | request headers |
| `proxy` | body | `object` | yes | proxy info |
| `proxy.country` | body | `string` | no | proxy country, see more in [Scrapeless proxy documentation](https://docs.scrapeless.com/en/proxies/features/proxy/) |
| `proxy.url` | body | `string` | no | proxy url |
