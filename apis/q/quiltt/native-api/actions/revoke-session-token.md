# Revoke Session Token with Quiltt

## Endpoint

- **Method:** `DELETE`
- **Path:** `https://auth.quiltt.io/v1/users/session`
- **Base URL:** `https://api.quiltt.io`
- **Official documentation:** [Revoke Session Token](https://www.quiltt.dev/authentication/managing-session-tokens)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sessionToken` | body | `string` | yes | Session token to revoke. |
