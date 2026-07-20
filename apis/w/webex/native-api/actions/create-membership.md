# Create Membership with Webex

Creates a new membership in Webex.

## Endpoint

- **Method:** `POST`
- **Path:** `/memberships`
- **Base URL:** `https://webexapis.com/v1`
- **Official documentation:** [Create Membership](https://developer.webex.com/messaging/docs/api/v1/memberships/create-a-membership)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `roomId` | body | `string` | yes | Room to add the member to. |
| `personEmail` | body | `string` | yes | Email address of the member to add. |
