# Update Membership with Webex

Updates an existing membership in Webex.

## Endpoint

- **Method:** `PUT`
- **Path:** `/memberships/:membershipId`
- **Base URL:** `https://webexapis.com/v1`
- **Official documentation:** [Update Membership](https://developer.webex.com/messaging/docs/api/v1/memberships/update-a-membership)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `membershipId` | path | `string` | yes | Membership identifier. |
| `isModerator` | body | `boolean` | yes | Whether the member is a moderator. |
