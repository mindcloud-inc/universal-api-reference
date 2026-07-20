# Update Webhook with BulkSMS

Updates an existing webhook in BulkSMS.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks/:id`
- **Base URL:** `https://api.bulksms.com/v1`
- **Official documentation:** [Update Webhook](https://www.bulksms.com/developer/json/v1/#tag/webhooks/POST/webhooks/{id})

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The webhook ID to update. |
| `name` | body | `string` | yes | Webhook name. Names must be unique. |
| `url` | body | `string` | yes | Webhook destination URL. Must start with http or https. |
| `triggerScope` | body | `list` | yes | Webhook trigger scope: SENT or RECEIVED. Accepted values: `0`, `1`. |
| `contactEmailAddress` | body | `string` | no | Email address for webhook invocation problem notifications. |
| `invokeOption` | body | `list` | no | Whether BulkSMS invokes the webhook with one message or many messages. Accepted values: `0`, `1`. |
| `active` | body | `boolean` | no | Whether the webhook should be active after update. |
| `onWebApp` | body | `boolean` | no | Whether to show the webhook in the BulkSMS web app. |
