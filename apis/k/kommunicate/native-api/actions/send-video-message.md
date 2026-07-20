# Send Video Message with Kommunicate

Creates a video message in Kommunicate.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/ws/message/v2/send`
- **Base URL:** `https://services.kommunicate.io`
- **Official documentation:** [Send Video Message](https://docs.kommunicate.io/docs/message-types#videos--youtube)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `groupId` | body | `string` | yes |
| `message` | body | `string` | yes |
| `fromUserName` | body | `string` | yes |
| `payloadJson` | body | `string` | yes |
