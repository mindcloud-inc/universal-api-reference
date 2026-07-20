# Update User Webhook with Zeplin

Updates an existing user webhook in Zeplin.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/users/me/webhooks/{webhook_id}`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [Update User Webhook](https://docs.zeplin.dev/reference/updateuserwebhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhook_id` | path | `string` | yes | Webhook id |
| `url` | body | `string` | yes | The URL of the webhook |
| `name` | body | `string` | yes | The name of the webhook |
| `secret` | body | `string` | yes | The secret to be used to generate signatures for webhook requests |
| `status` | body | `string` | yes | The status of the webhook |
| `project_ids[]` | body | `array<string>` | yes | The project ids of the webhook |
| `styleguide_ids[]` | body | `array<string>` | yes | The styleguide ids of the webhook |
| `events[]` | body | `array<string>` | yes | The events of the webhook |
