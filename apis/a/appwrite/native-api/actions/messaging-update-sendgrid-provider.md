# Update Sendgrid provider with Appwrite

Updates the sendgrid provider in your Appwrite project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/messaging/providers/sendgrid/{providerId}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update Sendgrid provider](https://appwrite.io/docs/references/cloud/server-rest/messaging)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `providerId` | path | `string` | yes | Provider ID. |
| `name` | body | `string` | no | Provider name. |
| `enabled` | body | `boolean` | no | Set as enabled. |
| `apiKey` | body | `string` | no | Sendgrid API key. |
| `fromName` | body | `string` | no | Sender Name. |
| `fromEmail` | body | `string` | no | Sender email address. |
| `replyToName` | body | `string` | no | Name set in the Reply To field for the mail. Default value is Sender Name. |
| `replyToEmail` | body | `string` | no | Email set in the Reply To field for the mail. Default value is Sender Email. |
