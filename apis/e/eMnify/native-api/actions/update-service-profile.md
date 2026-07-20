# Update Service Profile with EMnify

Updates an existing service profile in EMnify.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/service_profile/:profile_id`
- **Base URL:** `https://cdn.emnify.net/api/v1`
- **Official documentation:** [Update Service Profile](https://docs.emnify.com/developers/api/service-profiles/service-profile-by-profile-id-patch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `auth_token` | body | `string` | yes | Auth token from Retrieve Authentication Token. |
| `profile_id` | path | `number` | yes | Service profile ID. |
| `name` | body | `string` | no | Updated service profile name. |
| `description` | body | `string` | no | Updated service profile description. |
| `allowed_4g` | body | `boolean` | no | Allow 4G/LTE and LTE-M connectivity. |
| `apply_data_quota` | body | `boolean` | no | Apply data quota limits. |
| `id` | body | `number` | no | Breakout region ID. |
| `id` | body | `number` | no | DNS configuration ID. |
