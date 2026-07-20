# Share Session with Didit

Creates a share token for a session in Didit.

## Endpoint

- **Method:** `POST`
- **Path:** `https://verification.didit.me/v3/session/{sessionId}/share/`
- **Base URL:** `https://verification.didit.me/v3`
- **Official documentation:** [Share Session](https://docs.didit.me/sessions-api/share-session/share)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `for_application_id` | body | `string` | yes |
| `sessionId` | path | `string` | yes |
| `ttl_in_seconds` | body | `number` | no |
