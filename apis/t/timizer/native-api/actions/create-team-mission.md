# Create Team Mission with Timizer

Creates a team mission in Timizer.

## Endpoint

- **Method:** `POST`
- **Path:** `/app/admin-teams/:teamId/missions`
- **Base URL:** `https://api.timizer.io`
- **Official documentation:** [Create Team Mission](https://api-doc.timizer.io)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | path | `number` | yes | ID of the team. |
| `name` | body | `string` | no | Name of the mission. |
| `type` | body | `list` | no | Mission type. Accepted values: `mission`, `project`. |
| `id` | body | `number` | no | Optional mission ID. |
| `customId` | body | `string` | no | Optional mission custom ID. |
| `clientId` | body | `number` | no | ID of the client. |
| `clientContactId` | body | `number` | no | Optional client contact ID. |
| `contractClientId` | body | `number` | no | Optional contract client ID. |
| `contractClientContactId` | body | `number` | no | Optional contract client contact ID. |
| `teamMemberLinkIds[]` | body | `array<number>` | no | Team member link IDs assigned to the mission. |
| `start` | body | `date` | no | Optional mission start datetime. |
| `end` | body | `date` | no | Optional mission end datetime. |
| `durationType` | body | `list` | no | Duration type for the mission. Accepted values: `day`, `hour`. |
| `durationValue` | body | `number` | no | Duration value. In seconds when durationType is hour. |
| `availableTagIds[]` | body | `array<number>` | no | Tag IDs available on the mission. |
| `isActive` | body | `boolean` | no | Whether the mission is active. |
| `clientSignatureRequired` | body | `boolean` | no | Whether client signature is required. |
| `additionalReceiver` | body | `string` | no | Optional email address receiving signed activity reports. |
| `purchaseOrder` | body | `string` | no | Optional purchase order reference. |
| `note` | body | `string` | no | Optional mission note. |
