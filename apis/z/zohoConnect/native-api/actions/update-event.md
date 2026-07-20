# Update Event with Zoho Connect

Updates an existing event in Zoho Connect.

## Endpoint

- **Method:** `POST`
- **Path:** `/pulse/api/updateEvent`
- **Base URL:** `https://connect.zoho.com`
- **Official documentation:** [Update Event](https://www.zoho.com/connect/api/update-event.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scopeID` | query | `string` | yes | — |
| `streamId` | query | `string` | yes | — |
| `title` | query | `string` | yes | — |
| `desc` | query | `string` | no | — |
| `location` | query | `string` | no | — |
| `fields` | query | `string` | no | Comma-separated file IDs uploaded through Zoho's file upload API. Up to 10 files per event. Send multiple values as a string separated by `,`. |
| `startYear` | query | `number` | yes | — |
| `startMonth` | query | `number` | yes | — |
| `startDate` | query | `number` | yes | — |
| `startHour` | query | `number` | yes | — |
| `startMin` | query | `number` | yes | — |
| `endYear` | query | `number` | yes | — |
| `endMonth` | query | `number` | yes | — |
| `endDate` | query | `number` | yes | — |
| `endHour` | query | `number` | yes | — |
| `endMin` | query | `number` | yes | — |
| `allDay` | query | `boolean` | no | — |
| `intervalDay` | query | `number` | no | — |
| `intervalMinute` | query | `number` | no | — |
| `intervalHour` | query | `number` | no | — |
| `invitedMembers` | query | `string` | no | Send multiple values as a string separated by `,`. |
| `invitedGroups` | query | `string` | no | Groups to be invited to the event. Separate multiple groups by a comma. Send multiple values as a string separated by `,`. |
| `deleteMemInvitees` | query | `string` | no | Removed invitees. Separate multiple members by a comma. Send multiple values as a string separated by `,`. |
| `deleteGrpInvitees` | query | `string` | no | Removed groups that are invited. Separate multiple groups by a comma. Send multiple values as a string separated by `,`. |
