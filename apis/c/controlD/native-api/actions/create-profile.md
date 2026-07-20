# Create Profile with Control D

Creates a profile in Control D.

## Endpoint

- **Method:** `POST`
- **Path:** `/profiles`
- **Base URL:** `https://api.controld.com`
- **Official documentation:** [Create Profile](https://docs.controld.com/reference/post_profiles)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name of the new profile |
| `clone_profile_id` | body | `string` | no | Primary key of profile to clone. If ommited, a blank profile is created. |
