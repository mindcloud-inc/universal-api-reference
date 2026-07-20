# Update Mailgun provider with Appwrite

Updates the mailgun provider in your Appwrite project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/messaging/providers/mailgun/{providerId}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update Mailgun provider](https://appwrite.io/docs/references/cloud/server-rest/messaging)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `providerId` | path | `string` | yes | Provider ID. |
| `name` | body | `string` | no | Provider name. |
| `apiKey` | body | `string` | no | Mailgun API Key. |
| `domain` | body | `string` | no | Mailgun Domain. |
| `isEuRegion` | body | `boolean` | no | Set as EU region. |
| `enabled` | body | `boolean` | no | Set as enabled. |
| `fromName` | body | `string` | no | Sender Name. |
| `fromEmail` | body | `string` | no | Sender email address. |
| `replyToName` | body | `string` | no | Name set in the reply to field for the mail. Default value is sender name. |
| `replyToEmail` | body | `string` | no | Email set in the reply to field for the mail. Default value is sender email. |
