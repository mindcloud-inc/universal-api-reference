# Send List Template Message with Kommunicate

Creates a list template message in Kommunicate.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/ws/message/v2/send`
- **Base URL:** `https://services.kommunicate.io`
- **Official documentation:** [Send List Template Message](https://docs.kommunicate.io/docs/message-types#list-template)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `groupId` | body | `string` | yes |
| `message` | body | `string` | yes |
| `fromUserName` | body | `string` | yes |
| `payload` | body | `object` | yes |
