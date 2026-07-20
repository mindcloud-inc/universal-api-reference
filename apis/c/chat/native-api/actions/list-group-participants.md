# List Group Participants with 2Chat

Retrieves WhatsApp group participants from 2Chat.

## Endpoint

- **Method:** `GET`
- **Path:** `/whatsapp/group/:group_uuid`
- **Base URL:** `https://api.p.2chat.io/open`
- **Official documentation:** [List Group Participants](https://developers.2chat.co/docs/API/WhatsApp/Web/groups/list-whatsapp-group-participants)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group_uuid` | path | `string` | yes | The UUID of the WhatsApp group. |
