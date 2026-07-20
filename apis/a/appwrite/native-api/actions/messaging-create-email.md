# Create email with Appwrite

Creates a new email in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/messaging/messages/email`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create email](https://appwrite.io/docs/references/cloud/server-rest/messaging)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `attachments` | body | `string` | no | Array of compound ID strings of bucket IDs and file IDs to be attached to the email. They should be formatted as <BUCKET_ID>:<FILE_ID>. |
| `bcc` | body | `string` | no | Array of target IDs to be added as BCC. |
| `cc` | body | `string` | no | Array of target IDs to be added as CC. |
| `messageId` | body | `string` | yes | Message ID. Choose a custom ID or generate a random ID with `ID.unique()`. Valid chars are a-z, A-Z, 0-9, period, hyphen, and underscore. Can't start with a special char. Max length is 36 chars. |
| `targets` | body | `string` | no | List of Targets IDs. |
| `topics` | body | `string` | no | List of Topic IDs. |
| `users` | body | `string` | no | List of User IDs. |
| `subject` | body | `string` | yes | Email Subject. |
| `content` | body | `string` | yes | Email Content. |
| `topics[]` | body | `array<string>` | no | List of Topic IDs. |
| `users[]` | body | `array<string>` | no | List of User IDs. |
| `targets[]` | body | `array<string>` | no | List of Targets IDs. |
| `cc[]` | body | `array<string>` | no | Array of target IDs to be added as CC. |
| `bcc[]` | body | `array<string>` | no | Array of target IDs to be added as BCC. |
| `attachments[]` | body | `array<string>` | no | Array of compound ID strings of bucket IDs and file IDs to be attached to the email. They should be formatted as <BUCKET_ID>:<FILE_ID>. |
| `draft` | body | `boolean` | no | Is message a draft |
| `html` | body | `boolean` | no | Is content of type HTML |
| `scheduledAt` | body | `string` | no | Scheduled delivery time for message in [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) format. DateTime value must be in future. |
