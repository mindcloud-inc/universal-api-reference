# Send Email with Rillion Prime Web Service

Send an email through Rillion Prime. Side-effectful — Prime delivers the email to its recipients.

## Endpoint

- **Method:** `POST`
- **Base URL:** `{baseUrl}`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `MessageItem` | body | `object` | yes | Fill in the fields below, or use Use Variables ({}) on this object to map the whole payload from a previous step. |
| `MessageItem.EmailFrom` | body | `string` | no | — |
| `MessageItem.EmailTo` | body | `string` | no | — |
| `MessageItem.EmailCc` | body | `string` | no | — |
| `MessageItem.Subject` | body | `string` | no | — |
| `MessageItem.Message` | body | `string` | no | — |
| `MessageItem.Source` | body | `string` | no | — |
