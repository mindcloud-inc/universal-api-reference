# Retrieve Service Profile with EMnify

Retrieves a service profile from EMnify.

## Endpoint

- **Method:** `GET`
- **Path:** `/service_profile/:profile_id`
- **Base URL:** `https://cdn.emnify.net/api/v1`
- **Official documentation:** [Retrieve Service Profile](https://docs.emnify.com/developers/api/service-profiles/service-profile-by-profile-id-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `auth_token` | body | `string` | yes | Auth token from Retrieve Authentication Token. |
| `profile_id` | path | `number` | yes | Service profile ID. |
