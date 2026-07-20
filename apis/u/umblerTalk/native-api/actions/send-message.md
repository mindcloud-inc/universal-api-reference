# Send Message with Umbler Talk

Creates a message in Umbler Talk.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/messages/`
- **Base URL:** `https://app-utalk.umbler.com/api`
- **Official documentation:** [Send Message](https://app-utalk.umbler.com/api/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chatId` | body | `string` | yes | The chat ID. |
| `message` | body | `string` | no | Message text. |
| `organizationId` | body | `string` | yes | The organization ID. |
