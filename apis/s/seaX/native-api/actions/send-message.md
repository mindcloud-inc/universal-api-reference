# Send Message with SeaX

Sends an SMS or MMS message from SeaX.

## Endpoint

- **Method:** `POST`
- **Path:** `/send_message`
- **Base URL:** `https://seax.seasalt.ai/seax-api/api/v1/workspace/{workspaceId}`
- **Official documentation:** [Send Message](https://api.seasalt.ai/seax/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact` | body | `object` | yes | Contact payload for the message recipient. |
| `message` | body | `string` | yes | Message body. |
| `phone_id` | body | `string` | yes | Phone identifier to send from. |
