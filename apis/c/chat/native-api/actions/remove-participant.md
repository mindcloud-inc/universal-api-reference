# Remove Participant with 2Chat

Updates a WhatsApp group in 2Chat by removing participants.

## Endpoint

- **Method:** `POST`
- **Path:** `/whatsapp/group/:group_uuid/remove-participant`
- **Base URL:** `https://api.p.2chat.io/open`
- **Official documentation:** [Remove Participant](https://developers.2chat.co/docs/API/WhatsApp/Web/groups/remove-participant)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group_uuid` | path | `string` | yes | The UUID of the WhatsApp group. |
| `from_number` | body | `string` | yes | The WhatsApp number connected to 2Chat that removes participants. |
| `participants[]` | body | `array<string>` | yes | The phone numbers to remove from the group. |
