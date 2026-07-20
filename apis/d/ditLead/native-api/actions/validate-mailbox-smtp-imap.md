# Validate Mailbox SMTP IMAP with DitLead

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/mailbox/validate`
- **Base URL:** `https://api.ditlead.com`
- **Official documentation:** [Validate Mailbox SMTP IMAP](https://ditlead.com/developer/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `imap.host` | body | `string` | no |
| `imap.password` | body | `string` | no |
| `imap.port` | body | `string` | no |
| `imap.username` | body | `string` | no |
| `smtp.emailAddress` | body | `string` | no |
| `smtp.host` | body | `string` | no |
| `smtp.password` | body | `string` | no |
| `smtp.port` | body | `string` | no |
| `smtp.secure` | body | `boolean` | no |
| `smtp.username` | body | `string` | no |
