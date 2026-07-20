# Add contacts in bulk to a group with Maildrip

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/contacts/bulk`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Add contacts in bulk to a group](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | body | `string` | no | — |
| `contacts[]` | body | `array<object>` | no | Send multiple values as a array. |
| `overwrite` | body | `boolean` | no | — |
