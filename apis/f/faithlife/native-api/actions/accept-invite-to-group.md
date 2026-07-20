# Accept Invite To Group with Faithlife

Accepts a group invite in Faithlife.

## Endpoint

- **Method:** `POST`
- **Path:** `/invites/:inviteId/accept`
- **Base URL:** `https://accountsapi.logos.com/v2`
- **Official documentation:** [Accept Invite To Group](https://developer.faithlife.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inviteId` | path | `string` | yes | The pending Faithlife invite ID to accept. |
