# Search CDX Captures with Wayback Machine

Finds archived captures in the Wayback Machine CDX index.

## Endpoint

- **Method:** `GET`
- **Path:** `https://web.archive.org/cdx/search/cdx`
- **Base URL:** `https://archive.org`
- **Official documentation:** [Search CDX Captures](https://github.com/internetarchive/wayback/blob/master/wayback-cdx-server/README.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | URL, host, prefix, or domain to search in the CDX capture index. |
| `matchType` | query | `list` | no | Optional URL match scope: exact, prefix, host, or domain. Accepted values: `0`, `1`, `2`, `3`. |
| `from` | query | `string` | no | Optional inclusive start timestamp, using 1 to 14 digits in yyyyMMddhhmmss order. |
| `to` | query | `string` | no | Optional inclusive end timestamp, using 1 to 14 digits in yyyyMMddhhmmss order. |
| `limit` | query | `number` | no | Maximum number of CDX rows to return. |
