# Create Webhook with Flexmail

Creates a new webhook in Flexmail.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks`
- **Base URL:** `https://api.flexmail.eu`
- **Official documentation:** [Create Webhook](https://api.flexmail.eu/documentation/#post-/webhooks)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `event_name` | body | `string` | yes |
| `target_url` | body | `string` | yes |
| `verification_token` | body | `string` | no |
