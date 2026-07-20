# List ratelimit overrides with Unkey

Retrieves rate limit overrides from Unkey.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/ratelimit.listOverrides`
- **Base URL:** `https://api.unkey.com`
- **Official documentation:** [List ratelimit overrides](https://unkey.com/docs/api-reference/ratelimit/list-ratelimit-overrides)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `namespace` | body | `string` | yes |
