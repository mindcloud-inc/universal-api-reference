# Update Domain 404 Check with Prerender.io

Updates a domain 404 check in Prerender.io.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v3/domain-404-check/{id}`
- **Base URL:** `https://api.prerender.io`
- **Official documentation:** [Update Domain 404 Check](https://api.prerender.io/v3/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `enabled` | body | `boolean` | yes |
| `id` | path | `number` | yes |
| `revisitInterval` | body | `number` | yes |
| `url` | body | `string` | yes |
