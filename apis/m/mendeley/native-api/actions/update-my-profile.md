# Update My Profile with Mendeley

## Endpoint

- **Method:** `PATCH`
- **Path:** `/profiles/me`
- **Base URL:** `https://api.mendeley.com`
- **Official documentation:** [Update My Profile](https://dev.mendeley.com/methods/#updating-the-logged-in-user%27s-profile)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.mendeley-profiles.1+json` |
| `Content-Type` | `application/vnd.mendeley-profile-amendment.1+json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `academic_status` | body | `string` | no | Academic status value for the profile. |
| `biography` | body | `string` | no | Short profile biography. |
| `title` | body | `string` | no | Profile title. |
