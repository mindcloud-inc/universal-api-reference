# Update Profile with Quiltt

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/profiles/:profileId`
- **Base URL:** `https://api.quiltt.io`
- **Official documentation:** [Update Profile](https://www.quiltt.dev/api/profiles)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | Updated profile email address. |
| `name` | body | `string` | no | Updated profile display name. |
| `phone` | body | `string` | no | Updated profile phone number. |
| `profileId` | path | `string` | yes | Quiltt profile ID. |
