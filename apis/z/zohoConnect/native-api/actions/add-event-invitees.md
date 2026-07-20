# Add Event Invitees with Zoho Connect

Adds invitees to an event in Zoho Connect.

## Endpoint

- **Method:** `POST`
- **Path:** `/pulse/api/addEventInvitees`
- **Base URL:** `https://connect.zoho.com`
- **Official documentation:** [Add Event Invitees](https://www.zoho.com/connect/api/add-event-invitees.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scopeID` | query | `string` | yes | — |
| `streamId` | query | `string` | yes | — |
| `invitedMembers` | query | `string` | yes | Send multiple values as a string separated by `,`. |
| `invitedGroups` | query | `string` | no | Send multiple values as a string separated by `,`. |
