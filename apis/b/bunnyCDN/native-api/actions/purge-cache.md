# Purge Cache with BunnyCDN

Purges cached content from a BunnyCDN pull zone.

## Endpoint

- **Method:** `POST`
- **Path:** `/pullzone/:id/purgeCache`
- **Base URL:** `https://api.bunny.net`
- **Official documentation:** [Purge Cache](https://docs.bunny.net/reference/bunnynet-api-overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Bunny pull zone ID. |
