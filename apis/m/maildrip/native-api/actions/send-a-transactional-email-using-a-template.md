# Send a transactional email using a template with Maildrip

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/emails/transaction/{emailId}`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Send a transactional email using a template](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emailId` | path | `string` | yes | ID of the email template |
| `email_address` | body | `string` | no | — |
| `name` | body | `string` | no | — |
| `variables` | body | `object` | no | — |
| `provider` | body | `string` | no | Email service provider to use |
