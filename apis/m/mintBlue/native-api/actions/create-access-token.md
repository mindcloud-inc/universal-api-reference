# Create Access Token with mintBlue

Creates a new access token in mintBlue.

## Endpoint

- **Method:** `POST`
- **Path:** `/sdk/latest`
- **Base URL:** `https://api.mintblue.com`
- **Official documentation:** [Create Access Token](https://mintblue.gitlab.io/sdk/classes/Mintblue.html#createAccesstoken)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `params.name` | body | `string` | yes | Access token name. |
| `params.expires_at` | body | `date` | no | Optional expiration date. |
| `params.scopes[]` | body | `array<string>` | no | Optional scopes array. |
