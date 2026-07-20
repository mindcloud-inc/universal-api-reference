# Issue Session Token with Quiltt

## Endpoint

- **Method:** `POST`
- **Path:** `https://auth.quiltt.io/v1/users/sessions`
- **Base URL:** `https://api.quiltt.io`
- **Official documentation:** [Issue Session Token](https://www.quiltt.dev/authentication/issuing-session-tokens)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | body | `string` | yes | Existing Quiltt profile ID to issue a session token for. |
