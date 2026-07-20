# Create SMTP provider with Appwrite

Creates a new SMTP provider in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/messaging/providers/smtp`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create SMTP provider](https://appwrite.io/docs/references/cloud/server-rest/messaging)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `providerId` | body | `string` | yes | Provider ID. Choose a custom ID or generate a random ID with `ID.unique()`. Valid chars are a-z, A-Z, 0-9, period, hyphen, and underscore. Can't start with a special char. Max length is 36 chars. |
| `name` | body | `string` | yes | Provider name. |
| `host` | body | `string` | yes | SMTP hosts. Either a single hostname or multiple semicolon-delimited hostnames. You can also specify a different port for each host such as `smtp1.example.com:25;smtp2.example.com`. You can also specify encryption type, for example: `tls://smtp1.example.com:587;ssl://smtp2.example.com:465"`. Hosts will be tried in order. |
| `port` | body | `number` | no | The default SMTP server port. |
| `username` | body | `string` | no | Authentication username. |
| `password` | body | `string` | no | Authentication password. |
| `encryption` | body | `string` | no | Encryption type. Can be omitted, 'ssl', or 'tls' |
| `autoTLS` | body | `boolean` | no | Enable SMTP AutoTLS feature. |
| `mailer` | body | `string` | no | The value to use for the X-Mailer header. |
| `fromName` | body | `string` | no | Sender Name. |
| `fromEmail` | body | `string` | no | Sender email address. |
| `replyToName` | body | `string` | no | Name set in the reply to field for the mail. Default value is sender name. |
| `replyToEmail` | body | `string` | no | Email set in the reply to field for the mail. Default value is sender email. |
| `enabled` | body | `boolean` | no | Set as enabled. |
