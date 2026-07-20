# List Browser Profiles with Scrapeless

Retrieves browser profiles from Scrapeless.

## Endpoint

- **Method:** `GET`
- **Path:** `/browser/profiles`
- **Base URL:** `https://api.scrapeless.com`
- **Official documentation:** [List Browser Profiles](https://apidocs.scrapeless.com/api-19188053)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | profile name or id |
| `page` | query | `string` | yes | page number (1-based) |
| `pageSize` | query | `string` | yes | number of items per page |
