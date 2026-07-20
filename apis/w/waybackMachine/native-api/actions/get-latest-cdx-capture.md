# Get Latest CDX Capture with Wayback Machine

Retrieves the latest archived capture from the Wayback Machine CDX index.

## Endpoint

- **Method:** `GET`
- **Path:** `https://web.archive.org/cdx/search/cdx`
- **Base URL:** `https://archive.org`
- **Official documentation:** [Get Latest CDX Capture](https://github.com/internetarchive/wayback/blob/master/wayback-cdx-server/README.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | URL to find the latest public CDX capture for. |
