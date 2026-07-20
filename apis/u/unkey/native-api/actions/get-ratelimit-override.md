# Get ratelimit override with Unkey

Retrieves a rate limit override from Unkey.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/ratelimit.getOverride`
- **Base URL:** `https://api.unkey.com`
- **Official documentation:** [Get ratelimit override](https://unkey.com/docs/api-reference/ratelimit/get-ratelimit-override)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `identifier` | body | `string` | yes |
| `namespace` | body | `string` | yes |
