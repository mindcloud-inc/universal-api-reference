# Get Oldest CDX Capture with Wayback Machine

Retrieves the oldest archived capture from the Wayback Machine CDX index.

## Endpoint

- **Method:** `GET`
- **Path:** `https://web.archive.org/cdx/search/cdx`
- **Base URL:** `https://archive.org`
- **Official documentation:** [Get Oldest CDX Capture](https://github.com/internetarchive/wayback/blob/master/wayback-cdx-server/README.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | URL to find the oldest public CDX capture for. |
