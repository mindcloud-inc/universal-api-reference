# Update Profile with Browser Use

Updates an existing profile in Browser Use.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/profiles/:profile_id`
- **Base URL:** `https://api.browser-use.com/api/v3`
- **Official documentation:** [Update Profile](https://docs.browser-use.com/cloud/api-v3/profiles/update-profile)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Optional profile name. |
| `profile_id` | path | `string` | yes | Browser profile ID. |
| `userId` | body | `string` | no | Internal user identifier associated with the profile. |
