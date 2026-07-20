# Update Cached Content with Google AI Studio

Updates cached content expiration in Google AI Studio.

## Endpoint

- **Method:** `PATCH`
- **Path:** `v1beta/cachedContents/:cachedContentId`
- **Base URL:** `https://generativelanguage.googleapis.com`
- **Official documentation:** [Update Cached Content](https://ai.google.dev/api/caching#method:-cachedcontents.patch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cachedContentId` | path | `string` | yes | Full cached content resource name, for example `cachedContents/abc123`. |
| `updateMask` | query | `string` | yes | Comma-separated fields to update. Use `ttl` for TTL-only updates. |
| `ttl` | body | `string` | yes | New cache TTL duration, e.g. `7200s`. |
