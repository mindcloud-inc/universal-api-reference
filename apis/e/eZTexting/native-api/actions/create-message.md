# Create Message with EZ Texting

Creates a message in EZ Texting.

## Endpoint

- **Method:** `POST`
- **Path:** `/messages`
- **Base URL:** `https://a.eztexting.com/v1`
- **Official documentation:** [Create Message](https://developers.eztexting.com/reference/create_3-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyName` | body | `string` | no | Company name for the message |
| `fromNumber` | body | `string` | no | EZ Texting sender number |
| `groupIds[]` | body | `array<string>` | no | Recipient contact group IDs |
| `mediaFileId` | body | `string` | no | Existing media file ID |
| `mediaUrl` | body | `string` | no | Public media URL |
| `message` | body | `string` | no | Message text |
| `messageTemplateId` | body | `string` | no | Message template ID |
| `messageType` | body | `string` | no | Requested message type to send. Allowed values: SMS or MMS. |
| `sendAt` | body | `string` | no | Scheduled send time |
| `strictValidation` | body | `boolean` | no | Require strict recipient validation |
| `toNumbers[]` | body | `array<string>` | no | Recipient phone numbers |
