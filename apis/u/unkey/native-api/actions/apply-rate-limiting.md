# Apply rate limiting with Unkey

Applies a rate limit check in Unkey.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/ratelimit.limit`
- **Base URL:** `https://api.unkey.com`
- **Official documentation:** [Apply rate limiting](https://unkey.com/docs/api-reference/ratelimit/apply-rate-limiting)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `duration` | body | `number` | yes |
| `identifier` | body | `string` | yes |
| `limit` | body | `number` | yes |
| `namespace` | body | `string` | yes |
