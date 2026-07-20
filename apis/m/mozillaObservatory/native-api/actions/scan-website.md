# Scan website with Mozilla Observatory

Creates a new website scan in Mozilla Observatory.

## Endpoint

- **Method:** `POST`
- **Path:** `/scan`
- **Base URL:** `https://observatory-api.mdn.mozilla.net/api/v2`
- **Official documentation:** [Scan website](https://developer.mozilla.org/en-US/observatory/docs/faq)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `host` | query | `string` | yes | Hostname to scan. |
