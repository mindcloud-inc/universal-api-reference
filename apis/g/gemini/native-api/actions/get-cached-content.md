# Get Cached Content with Gemini

Retrieves a cached content resource from Gemini.

## Endpoint

- **Method:** `GET`
- **Path:** `v1beta/cachedContents/:cachedContentId`
- **Base URL:** `https://generativelanguage.googleapis.com`
- **Official documentation:** [Get Cached Content](https://ai.google.dev/api/caching#method:-cachedcontents.get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cachedContentId` | path | `string` | yes | Cached content ID segment (without `cachedContents/` prefix). |
