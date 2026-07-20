# Invite users with Statsig

Invites users to Statsig.

## Endpoint

- **Method:** `POST`
- **Path:** `/console/v1/users/invite`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Invite users](https://docs.statsig.com/api-reference/users/invite-users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `role` | body | `string` | yes | Request body field. |
| `emails` | body | `list` | yes | Request body field. |
| `teams` | body | `list` | no | Request body field. |
