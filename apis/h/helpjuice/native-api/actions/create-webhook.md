# Create Webhook with Helpjuice

Creates a new webhook in Helpjuice.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Create Webhook](https://help.helpjuice.com/api-v3/using-api-v3)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | The webhook callback URL. |
| `event` | body | `string` | yes | The Helpjuice webhook event, for example question_create. |
