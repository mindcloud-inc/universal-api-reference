# Update SMTP provider with Appwrite

Updates the SMTP provider in your Appwrite project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/messaging/providers/smtp/{providerId}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update SMTP provider](https://appwrite.io/docs/references/cloud/server-rest/messaging)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `providerId` | path | `string` | yes | Provider ID. |
| `name` | body | `string` | no | Provider name. |
| `host` | body | `string` | no | SMTP hosts. Either a single hostname or multiple semicolon-delimited hostnames. You can also specify a different port for each host such as `smtp1.example.com:25;smtp2.example.com`. You can also specify encryption type, for example: `tls://smtp1.example.com:587;ssl://smtp2.example.com:465"`. Hosts will be tried in order. |
| `port` | body | `number` | no | SMTP port. |
| `username` | body | `string` | no | Authentication username. |
| `password` | body | `string` | no | Authentication password. |
| `encryption` | body | `string` | no | Encryption type. Can be 'ssl' or 'tls' |
| `autoTLS` | body | `boolean` | no | Enable SMTP AutoTLS feature. |
| `mailer` | body | `string` | no | The value to use for the X-Mailer header. |
| `fromName` | body | `string` | no | Sender Name. |
| `fromEmail` | body | `string` | no | Sender email address. |
| `replyToName` | body | `string` | no | Name set in the Reply To field for the mail. Default value is Sender Name. |
| `replyToEmail` | body | `string` | no | Email set in the Reply To field for the mail. Default value is Sender Email. |
| `enabled` | body | `boolean` | no | Set as enabled. |
