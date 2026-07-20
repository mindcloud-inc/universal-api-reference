# Revoke User Sessions with Rownd Data Privacy

## Endpoint

- **Method:** `POST`
- **Path:** `/users/:user/signout`
- **Base URL:** `https://api.rownd.io/applications/{appId}`
- **Official documentation:** [Revoke User Sessions](https://docs.rownd.io/api-reference/user-sessions/app/revoke-user-sessions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user` | path | `string` | yes | Rownd user identifier. |
