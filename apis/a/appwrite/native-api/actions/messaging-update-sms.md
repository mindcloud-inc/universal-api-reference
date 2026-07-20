# Update SMS with Appwrite

Updates the SMS in your Appwrite project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/messaging/messages/sms/{messageId}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update SMS](https://appwrite.io/docs/references/cloud/server-rest/messaging)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messageId` | path | `string` | yes | Message ID. |
| `targets` | body | `string` | no | List of Targets IDs. |
| `topics` | body | `string` | no | List of Topic IDs. |
| `users` | body | `string` | no | List of User IDs. |
| `topics[]` | body | `array<string>` | no | List of Topic IDs. |
| `users[]` | body | `array<string>` | no | List of User IDs. |
| `targets[]` | body | `array<string>` | no | List of Targets IDs. |
| `content` | body | `string` | no | Email Content. |
| `draft` | body | `boolean` | no | Is message a draft |
| `scheduledAt` | body | `string` | no | Scheduled delivery time for message in [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) format. DateTime value must be in future. |
