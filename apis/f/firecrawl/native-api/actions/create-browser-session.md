# Create Browser Session with Firecrawl

Creates a browser session in Firecrawl.

## Endpoint

- **Method:** `POST`
- **Path:** `/browser`
- **Base URL:** `https://api.firecrawl.dev/v2`
- **Official documentation:** [Create Browser Session](https://docs.firecrawl.dev/api-reference/endpoint/browser-create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ttl` | body | `number` | no | Total time-to-live in seconds for the browser session |
| `activityTtl` | body | `number` | no | Time in seconds before the session is destroyed due to inactivity |
| `streamWebView` | body | `boolean` | no | Whether to stream a live view of the browser |
| `profile` | body | `object` | no | Persistent browser profile settings |
