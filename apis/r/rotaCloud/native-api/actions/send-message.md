# Send Message with RotaCloud

Sends a message in RotaCloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/messages`
- **Base URL:** `https://api.rotacloud.com`
- **Official documentation:** [Send Message](https://rotacloud.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message` | body | `string` | yes | Message body. |
| `subject` | body | `string` | yes | Message subject. |
| `users` | body | `number` | yes | Recipient user IDs. Send multiple values as a string separated by `,`. |
