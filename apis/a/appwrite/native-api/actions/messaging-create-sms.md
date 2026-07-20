# Create SMS with Appwrite

Creates SMS in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/messaging/messages/sms`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create SMS](https://appwrite.io/docs/references/cloud/server-rest/messaging)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messageId` | body | `string` | yes | Message ID. Choose a custom ID or generate a random ID with `ID.unique()`. Valid chars are a-z, A-Z, 0-9, period, hyphen, and underscore. Can't start with a special char. Max length is 36 chars. |
| `targets` | body | `string` | no | List of Targets IDs. |
| `topics` | body | `string` | no | List of Topic IDs. |
| `users` | body | `string` | no | List of User IDs. |
| `content` | body | `string` | yes | SMS Content. |
| `topics[]` | body | `array<string>` | no | List of Topic IDs. |
| `users[]` | body | `array<string>` | no | List of User IDs. |
| `targets[]` | body | `array<string>` | no | List of Targets IDs. |
| `draft` | body | `boolean` | no | Is message a draft |
| `scheduledAt` | body | `string` | no | Scheduled delivery time for message in [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) format. DateTime value must be in future. |
