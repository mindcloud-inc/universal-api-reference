# Create Webhook with Resend

Creates a new webhook in Resend.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks`
- **Base URL:** `https://api.resend.com`
- **Official documentation:** [Create Webhook](https://resend.com/docs/api-reference/webhooks/create-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `endpoint` | body | `string` | yes | The URL where webhook events will be sent |
| `events[]` | body | `array<string>` | yes | Array of event types to subscribe to Accepted values: `contact.created`, `contact.deleted`, `contact.updated`, `domain.created`, `domain.deleted`, `domain.updated`, `email.bounced`, `email.clicked`, `email.complained`, `email.delivered`, `email.delivery_delayed`, `email.failed`, `email.opened`, `email.received`, `email.scheduled`, `email.sent`, `email.suppressed`. Send multiple values as a array. |
