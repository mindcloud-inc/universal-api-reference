# Create Profile with Browser Use

Creates a profile in Browser Use.

## Endpoint

- **Method:** `POST`
- **Path:** `/profiles`
- **Base URL:** `https://api.browser-use.com/api/v3`
- **Official documentation:** [Create Profile](https://docs.browser-use.com/cloud/api-v3/profiles/create-profile)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Optional profile name. |
| `userId` | body | `string` | no | Internal user identifier associated with the profile. |
