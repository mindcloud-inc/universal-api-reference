# Update email with Appwrite

Updates the email in your Appwrite project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/messaging/messages/email/{messageId}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update email](https://appwrite.io/docs/references/cloud/server-rest/messaging)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `attachments` | body | `string` | no | Array of compound ID strings of bucket IDs and file IDs to be attached to the email. They should be formatted as <BUCKET_ID>:<FILE_ID>. |
| `bcc` | body | `string` | no | Array of target IDs to be added as BCC. |
| `cc` | body | `string` | no | Array of target IDs to be added as CC. |
| `messageId` | path | `string` | yes | Message ID. |
| `targets` | body | `string` | no | List of Targets IDs. |
| `topics` | body | `string` | no | List of Topic IDs. |
| `users` | body | `string` | no | List of User IDs. |
| `topics[]` | body | `array<string>` | no | List of Topic IDs. |
| `users[]` | body | `array<string>` | no | List of User IDs. |
| `targets[]` | body | `array<string>` | no | List of Targets IDs. |
| `subject` | body | `string` | no | Email Subject. |
| `content` | body | `string` | no | Email Content. |
| `draft` | body | `boolean` | no | Is message a draft |
| `html` | body | `boolean` | no | Is content of type HTML |
| `cc[]` | body | `array<string>` | no | Array of target IDs to be added as CC. |
| `bcc[]` | body | `array<string>` | no | Array of target IDs to be added as BCC. |
| `scheduledAt` | body | `string` | no | Scheduled delivery time for message in [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) format. DateTime value must be in future. |
| `attachments[]` | body | `array<string>` | no | Array of compound ID strings of bucket IDs and file IDs to be attached to the email. They should be formatted as <BUCKET_ID>:<FILE_ID>. |
