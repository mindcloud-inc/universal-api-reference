# Create Webhook with Documo

Creates a new webhook in Documo.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks`
- **Base URL:** `https://api.documo.com`
- **Official documentation:** [Create Webhook](https://docs.documo.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Webhook name. |
| `url` | body | `string` | yes | Webhook URL. |
| `events` | body | `string` | no | Webhook events payload. |
| `auth` | body | `string` | no | Basic auth in username:password format. |
| `accountId` | body | `string` | no | Account UUID. |
| `numberId` | body | `string` | no | Fax number UUID. |
| `notificationEmails` | body | `string` | no | Notification email recipients. |
