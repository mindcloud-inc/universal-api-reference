# Issue Session Token For New Profile with Quiltt

## Endpoint

- **Method:** `POST`
- **Path:** `https://auth.quiltt.io/v1/users/sessions`
- **Base URL:** `https://api.quiltt.io`
- **Official documentation:** [Issue Session Token For New Profile](https://www.quiltt.dev/authentication/issuing-session-tokens)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | New profile email address. |
| `name` | body | `string` | no | New profile display name. |
| `uuid` | body | `string` | no | Optional custom UUID for the new profile. |
