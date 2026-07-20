# Add Participant with 2Chat

Updates a WhatsApp group in 2Chat by adding participants.

## Endpoint

- **Method:** `POST`
- **Path:** `/whatsapp/group/:group_uuid/add-participant`
- **Base URL:** `https://api.p.2chat.io/open`
- **Official documentation:** [Add Participant](https://developers.2chat.co/docs/API/WhatsApp/Web/groups/add-participant)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group_uuid` | path | `string` | yes | The UUID of the WhatsApp group. |
| `from_number` | body | `string` | yes | The WhatsApp number connected to 2Chat that adds participants. |
| `participants[]` | body | `array<string>` | yes | The phone numbers to add to the group. |
