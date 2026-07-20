# Get Tariff Profile Details with EMnify

Retrieves tariff profile details from EMnify.

## Endpoint

- **Method:** `GET`
- **Path:** `/tariff_profile/:tariff_profile_id`
- **Base URL:** `https://cdn.emnify.net/api/v1`
- **Official documentation:** [Get Tariff Profile Details](https://docs.emnify.com/developers/api/tariff-profiles/tariff-profile-by-id-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `auth_token` | body | `string` | yes | Auth token from Retrieve Authentication Token. |
| `tariff_profile_id` | path | `number` | yes | Tariff profile ID. |
