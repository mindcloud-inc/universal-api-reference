# Reset Account User Authentication Method with Bridgit Bench

## Endpoint

- **Method:** `POST`
- **Path:** `/rp/api/v1/accounts/:accountId/users/:userId/reset-auth-method`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Reset Account User Authentication Method](https://developers.gobridgit.com/reference/accountusers_resetauthmethod)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The account that is currently calling this method. |
| `userId` | path | `number` | yes | The ID of the account user. |
