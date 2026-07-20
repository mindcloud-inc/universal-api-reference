# Create Invite with HeadshotPro

Creates a new invite in HeadshotPro.

## Endpoint

- **Method:** `POST`
- **Path:** `/organization/invites`
- **Base URL:** `https://server.headshotpro.com/api/v2`
- **Official documentation:** [Create Invite](https://www.headshotpro.com/api/invites)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email address to invite. |
| `teamId` | body | `string` | no | Optional team to assign when the invite is used. |
