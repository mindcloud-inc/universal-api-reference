# Delete ratelimit override with Unkey

Deletes a rate limit override from Unkey.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/ratelimit.deleteOverride`
- **Base URL:** `https://api.unkey.com`
- **Official documentation:** [Delete ratelimit override](https://unkey.com/docs/api-reference/ratelimit/delete-ratelimit-override)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `identifier` | body | `string` | yes |
| `namespace` | body | `string` | yes |
