# Cancel Invitation with Rollbar

Deletes an existing team invitation from Rollbar.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/invite/:inviteId`
- **Base URL:** `https://api.rollbar.com/api/1`
- **Official documentation:** [Cancel Invitation](https://docs.rollbar.com/reference/cancel-an-invitation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inviteId` | path | `number` | yes | Team invitation identifier |
