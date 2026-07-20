# Set ratelimit override with Unkey

Sets a rate limit override in Unkey.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/ratelimit.setOverride`
- **Base URL:** `https://api.unkey.com`
- **Official documentation:** [Set ratelimit override](https://unkey.com/docs/api-reference/ratelimit/set-ratelimit-override)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `duration` | body | `number` | yes |
| `identifier` | body | `string` | yes |
| `limit` | body | `number` | yes |
| `namespace` | body | `string` | yes |
