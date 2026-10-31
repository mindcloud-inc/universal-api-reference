# Send Account Invitation with Bridgit Bench

## Endpoint

- **Method:** `POST`
- **Path:** `/rp/api/v1/accounts/:accountId/invitations`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Send Account Invitation](https://developers.gobridgit.com/reference/accountinvitations_post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The ID of the account |
| `groupingPermissions[]` | body | `array<object>` | no | — |
| `groupingPermissions[].id` | body | `number` | yes | — |
| `groupingPermissions[].groupId` | body | `number` | yes | — |
| `email` | body | `string` | yes | Maximum length: 254. |
| `group` | body | `string` | yes | Maximum length: 50. |
