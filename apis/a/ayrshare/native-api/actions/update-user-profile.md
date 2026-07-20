# Update User Profile with Ayrshare

Updates an existing user profile in Ayrshare.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/profiles`
- **Base URL:** `https://api.ayrshare.com/api`
- **Official documentation:** [Update User Profile](https://www.ayrshare.com/docs/apis/profiles/update-profile)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `profileKey` | body | `string` | yes | Profile key for the user profile to update. |
| `title` | body | `string` | no | Updated profile title. |
