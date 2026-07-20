# Update Domains Config with Prerender.io

Updates config for a domain in Prerender.io.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v3/domains/{domain}/config`
- **Base URL:** `https://api.prerender.io`
- **Official documentation:** [Update Domains Config](https://api.prerender.io/v3/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `cacheLifetimeHours` | body | `number` | yes |
| `domain` | path | `string` | yes |
| `onlyServeCacheHits` | body | `boolean` | yes |
| `slowRenderTriggerSeconds` | body | `number` | yes |
