# Create Resend provider with Appwrite

Creates a new resend provider in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/messaging/providers/resend`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create Resend provider](https://appwrite.io/docs/references/cloud/server-rest/messaging)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `providerId` | body | `string` | yes | Provider ID. Choose a custom ID or generate a random ID with `ID.unique()`. Valid chars are a-z, A-Z, 0-9, period, hyphen, and underscore. Can't start with a special char. Max length is 36 chars. |
| `name` | body | `string` | yes | Provider name. |
| `apiKey` | body | `string` | no | Resend API key. |
| `fromName` | body | `string` | no | Sender Name. |
| `fromEmail` | body | `string` | no | Sender email address. |
| `replyToName` | body | `string` | no | Name set in the reply to field for the mail. Default value is sender name. |
| `replyToEmail` | body | `string` | no | Email set in the reply to field for the mail. Default value is sender email. |
| `enabled` | body | `boolean` | no | Set as enabled. |
