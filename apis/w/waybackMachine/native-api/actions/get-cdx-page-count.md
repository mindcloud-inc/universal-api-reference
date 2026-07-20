# Get CDX Page Count with Wayback Machine

Retrieves the CDX result page count for a Wayback query.

## Endpoint

- **Method:** `GET`
- **Path:** `https://web.archive.org/cdx/search/cdx`
- **Base URL:** `https://archive.org`
- **Official documentation:** [Get CDX Page Count](https://github.com/internetarchive/wayback/blob/master/wayback-cdx-server/README.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | URL, host, prefix, or domain to estimate CDX result pages for. |
| `pageSize` | query | `number` | no | Optional CDX page size block count for page-count estimation. |
