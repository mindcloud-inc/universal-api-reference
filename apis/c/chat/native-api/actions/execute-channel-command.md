# Execute Channel Command with 2Chat

Updates a WhatsApp channel in 2Chat with a command.

## Endpoint

- **Method:** `POST`
- **Path:** `/whatsapp/channel/:channel_uuid/:command`
- **Base URL:** `https://api.p.2chat.io/open`
- **Official documentation:** [Execute Channel Command](https://developers.2chat.co/docs/API/WhatsApp/Web/channel/execute-channel-command)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel_uuid` | path | `string` | yes | The UUID of the WhatsApp channel connected to 2Chat. |
| `command` | path | `string` | yes | The command to execute for the channel, such as connect or disconnect. |
