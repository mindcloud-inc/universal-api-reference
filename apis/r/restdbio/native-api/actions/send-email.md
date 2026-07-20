# Send Email with Restdb.io

Sends an email through Restdb.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/mail`
- **Base URL:** `https://mindcloudstage0-7934.restdb.io`
- **Official documentation:** [Send Email](https://restdb.io/media/restdb-cheat-sheet.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company` | body | `string` | no | Optional company label shown in the email. |
| `html` | body | `string` | yes | HTML body to send. |
| `sendername` | body | `string` | no | Optional sender display name. |
| `subject` | body | `string` | yes | Email subject line. |
| `to` | body | `string` | yes | Recipient email address. |
