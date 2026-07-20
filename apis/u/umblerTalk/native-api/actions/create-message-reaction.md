# Create Message Reaction with Umbler Talk

Creates a message reaction in Umbler Talk.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/messages/reactions/`
- **Base URL:** `https://app-utalk.umbler.com/api`
- **Official documentation:** [Create Message Reaction](https://app-utalk.umbler.com/api/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emoji` | body | `string` | no | Emoji reaction. |
| `messageId` | body | `string` | yes | The message ID. |
| `organizationId` | body | `string` | yes | The organization ID. |
