# Create Cached Content with Google AI Studio

Creates a cached content entry in Google AI Studio.

## Endpoint

- **Method:** `POST`
- **Path:** `v1beta/cachedContents`
- **Base URL:** `https://generativelanguage.googleapis.com`
- **Official documentation:** [Create Cached Content](https://ai.google.dev/api/caching#method:-cachedcontents.create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `string` | yes | Required model name in the format `models/{model}`. |
| `contents[]` | body | `array<object>` | yes | Required content array to cache. |
| `displayName` | body | `string` | no | Optional display name for the cache entry. |
| `ttl` | body | `string` | no | Optional cache duration, e.g. `3600s`. |
