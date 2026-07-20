# Send Generic Card Message with Kommunicate

Creates a generic card message in Kommunicate.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/ws/message/v2/send`
- **Base URL:** `https://services.kommunicate.io`
- **Official documentation:** [Send Generic Card Message](https://docs.kommunicate.io/docs/message-types#generic-card)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `groupId` | body | `string` | yes |
| `message` | body | `string` | yes |
| `fromUserName` | body | `string` | yes |
| `card` | body | `object` | yes |
