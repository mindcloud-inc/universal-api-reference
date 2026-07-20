# Revoke Invite with HeadshotPro

Revokes an invite in HeadshotPro by email address.

## Endpoint

- **Method:** `POST`
- **Path:** `/organization/invites/revoke`
- **Base URL:** `https://server.headshotpro.com/api/v2`
- **Official documentation:** [Revoke Invite](https://www.headshotpro.com/api/invites)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email address of the invite to revoke. |
