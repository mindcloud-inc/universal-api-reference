# Create Webhook with Trustmary

Creates a new webhook in Trustmary.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks`
- **Base URL:** `https://api.trustmary.io/v1`
- **Official documentation:** [Create Webhook](https://help.trustmary.com/api#/paths/~1webhooks/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Webhook display name. |
| `hookUrl` | body | `string` | yes | Destination URL for webhook deliveries. |
| `events[]` | body | `array<string>` | yes | Webhook event types array. Send multiple values as a array. |
