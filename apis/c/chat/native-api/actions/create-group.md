# Create Group with 2Chat

Creates a WhatsApp group in 2Chat.

## Endpoint

- **Method:** `POST`
- **Path:** `/whatsapp/group/create`
- **Base URL:** `https://api.p.2chat.io/open`
- **Official documentation:** [Create Group](https://developers.2chat.co/docs/API/WhatsApp/Web/groups/create-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from_number` | body | `string` | yes | The WhatsApp number connected to 2Chat that creates the group. |
| `group.name` | body | `string` | yes | The name of the WhatsApp group to create. |
| `group.description` | body | `string` | no | An optional description for the WhatsApp group. |
| `group.participants[]` | body | `array<string>` | yes | The phone numbers to add to the new WhatsApp group. |
