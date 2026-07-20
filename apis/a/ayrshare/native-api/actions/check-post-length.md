# Check Post Length with Ayrshare

Checks post length against platform limits in Ayrshare.

## Endpoint

- **Method:** `POST`
- **Path:** `/post/checkPostWeight`
- **Base URL:** `https://api.ayrshare.com/api`
- **Official documentation:** [Check Post Length](https://www.ayrshare.com/docs/apis/validate/check-post-length)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `post` | body | `string` | yes | Post text to calculate weighted length for. |
| `platform` | body | `string` | no | Optional platform context for the post length check. |
