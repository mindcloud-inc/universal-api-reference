# Create User Webhook with Zeplin

Creates a new user webhook in Zeplin.

## Endpoint

- **Method:** `POST`
- **Path:** `/users/me/webhooks`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [Create User Webhook](https://docs.zeplin.dev/reference/createuserwebhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | The URL of the webhook |
| `name` | body | `string` | yes | The name of the webhook |
| `secret` | body | `string` | yes | The secret to be used to generate signatures for webhook requests |
| `status` | body | `object` | yes | The status of the webhook |
| `project_ids[]` | body | `array<string>` | yes | The project ids of the webhook |
| `styleguide_ids[]` | body | `array<string>` | yes | The styleguide ids of the webhook |
| `events[]` | body | `array<string>` | yes | The events of the webhook |
