# Remove contacts from a group or delete them entirely (asynchronous). with Maildrip

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/contacts/delete`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Remove contacts from a group or delete them entirely (asynchronous).](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | body | `string` | no | ID of the group from which contacts will be removed. Optional if contacts array is provided. Required if resetGroup is true. |
| `contacts[]` | body | `array<string>` | no | Array of contact IDs to remove or delete. Optional if groupId with resetGroup true is provided. Required otherwise. Send multiple values as a array. |
| `resetGroup` | body | `boolean` | no | If true, removes all contacts from the group (requires groupId). If false, removes only specified contacts from the group. |
