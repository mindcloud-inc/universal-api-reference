# Update Styleguide Webhook with Zeplin

Updates an existing styleguide webhook in Zeplin.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/styleguides/{styleguide_id}/webhooks/{webhook_id}`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [Update Styleguide Webhook](https://docs.zeplin.dev/reference/updatestyleguidewebhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `styleguide_id` | path | `string` | yes | Styleguide id |
| `webhook_id` | path | `string` | yes | Webhook id |
| `url` | body | `string` | yes | The URL of the webhook |
| `name` | body | `string` | yes | The name of the webhook |
| `secret` | body | `string` | yes | The secret to be used to generate signatures for webhook requests |
| `status` | body | `string` | yes | The status of the webhook |
| `events[]` | body | `array<string>` | yes | The events of the webhook |
