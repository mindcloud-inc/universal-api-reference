# Create Mailbox with DitLead

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/mailbox`
- **Base URL:** `https://api.ditlead.com`
- **Official documentation:** [Create Mailbox](https://ditlead.com/developer/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `firstName` | body | `string` | no | — |
| `firstName` | body | `string` | yes | Sender first name. |
| `imap` | body | `object` | yes | IMAP credentials object. |
| `imap.host` | body | `string` | no | — |
| `imap.password` | body | `string` | no | — |
| `imap.port` | body | `string` | no | — |
| `imap.username` | body | `string` | no | — |
| `lastName` | body | `string` | no | — |
| `lastName` | body | `string` | yes | Sender last name. |
| `smtp` | body | `object` | yes | SMTP credentials object. |
| `smtp.emailAddress` | body | `string` | no | — |
| `smtp.host` | body | `string` | no | — |
| `smtp.password` | body | `string` | no | — |
| `smtp.port` | body | `string` | no | — |
| `smtp.secure` | body | `boolean` | no | — |
| `smtp.username` | body | `string` | no | — |
