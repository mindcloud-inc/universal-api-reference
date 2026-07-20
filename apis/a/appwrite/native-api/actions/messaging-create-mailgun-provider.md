# Create Mailgun provider with Appwrite

Creates a new mailgun provider in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/messaging/providers/mailgun`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create Mailgun provider](https://appwrite.io/docs/references/cloud/server-rest/messaging)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `providerId` | body | `string` | yes | Provider ID. Choose a custom ID or generate a random ID with `ID.unique()`. Valid chars are a-z, A-Z, 0-9, period, hyphen, and underscore. Can't start with a special char. Max length is 36 chars. |
| `name` | body | `string` | yes | Provider name. |
| `apiKey` | body | `string` | no | Mailgun API Key. |
| `domain` | body | `string` | no | Mailgun Domain. |
| `isEuRegion` | body | `boolean` | no | Set as EU region. |
| `fromName` | body | `string` | no | Sender Name. |
| `fromEmail` | body | `string` | no | Sender email address. |
| `replyToName` | body | `string` | no | Name set in the reply to field for the mail. Default value is sender name. Reply to name must have reply to email as well. |
| `replyToEmail` | body | `string` | no | Email set in the reply to field for the mail. Default value is sender email. Reply to email must have reply to name as well. |
| `enabled` | body | `boolean` | no | Set as enabled. |
