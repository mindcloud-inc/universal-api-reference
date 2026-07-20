# Send Form Template Message with Kommunicate

Creates a form template message in Kommunicate.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/ws/message/v2/send`
- **Base URL:** `https://services.kommunicate.io`
- **Official documentation:** [Send Form Template Message](https://docs.kommunicate.io/docs/message-types#form-template)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `groupId` | body | `string` | yes |
| `message` | body | `string` | yes |
| `fromUserName` | body | `string` | yes |
| `payloadJson` | body | `string` | yes |
