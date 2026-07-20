# Update Webhook with Documo

Updates an existing webhook in Documo.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/webhooks/:webhookId`
- **Base URL:** `https://api.documo.com`
- **Official documentation:** [Update Webhook](https://docs.documo.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhookId` | path | `string` | yes | Webhook UUID. |
| `name` | body | `string` | no | Webhook name. |
| `url` | body | `string` | no | Webhook URL. |
| `events` | body | `string` | no | Webhook events payload. |
| `auth` | body | `string` | no | Basic auth in username:password format. |
| `accountId` | body | `string` | no | Account UUID. |
| `numberId` | body | `string` | no | Fax number UUID. |
| `notificationEmails` | body | `string` | no | Notification email recipients. |
