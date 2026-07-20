# Send Auto Suggestion Message with Kommunicate

Creates an auto suggestion message in Kommunicate.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/ws/message/v2/send`
- **Base URL:** `https://services.kommunicate.io`
- **Official documentation:** [Send Auto Suggestion Message](https://docs.kommunicate.io/docs/message-types#autosuggestions-in-your-chat-box)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `groupId` | body | `string` | yes |
| `message` | body | `string` | yes |
| `fromUserName` | body | `string` | yes |
| `placeholder` | body | `string` | no |
| `source` | body | `object` | yes |
