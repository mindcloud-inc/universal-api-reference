# Login With Magic Link with Florm

Logs into Florm with a magic link.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/auth/magic-links`
- **Base URL:** `https://api.florm.io`
- **Official documentation:** [Login With Magic Link](https://api.florm.io/docs#/default/login_magic_link_v1_auth_magic_links_put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `guid` | body | `string` | yes | GUID of the Florm magic-link challenge. |
| `code` | body | `number` | yes | 4-digit code from the Florm magic link email. |
| `language` | body | `string` | no | Language code for the Florm login flow. |
