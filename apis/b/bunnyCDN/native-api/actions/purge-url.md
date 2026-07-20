# Purge URL with BunnyCDN

Purges a URL from the BunnyCDN cache.

## Endpoint

- **Method:** `POST`
- **Path:** `/purge`
- **Base URL:** `https://api.bunny.net`
- **Official documentation:** [Purge URL](https://docs.bunny.net/reference/bunnynet-api-overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | The URL that will be purged from cache. |
