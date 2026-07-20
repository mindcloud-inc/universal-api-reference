# Create Domain 404 Check with Prerender.io

Creates a domain 404 check in Prerender.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/domain-404-check`
- **Base URL:** `https://api.prerender.io`
- **Official documentation:** [Create Domain 404 Check](https://api.prerender.io/v3/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `revisitInterval` | body | `number` | yes |
| `url` | body | `string` | yes |
