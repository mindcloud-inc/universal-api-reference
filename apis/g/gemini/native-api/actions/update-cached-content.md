# Update Cached Content with Gemini

Updates a cached content resource in Gemini.

## Endpoint

- **Method:** `PATCH`
- **Path:** `v1beta/cachedContents/:cachedContentId`
- **Base URL:** `https://generativelanguage.googleapis.com`
- **Official documentation:** [Update Cached Content](https://ai.google.dev/api/caching#method:-cachedcontents.patch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cachedContentId` | path | `string` | yes | Cached content ID segment (without `cachedContents/` prefix). |
| `updateMask` | query | `string` | yes | Comma-separated fields to update. Use `ttl` for TTL-only updates. |
| `ttl` | body | `string` | yes | New cache TTL duration, e.g. `7200s`. |
