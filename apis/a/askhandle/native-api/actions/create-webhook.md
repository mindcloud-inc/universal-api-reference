# Create Webhook with AskHandle

Creates a new webhook in AskHandle.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks/`
- **Base URL:** `https://dashboard.askhandle.com/api/v1`
- **Official documentation:** [Create Webhook](https://dashboard.askhandle.com/api/v1/docs/api_reference.html#webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event` | body | `string` | yes | Webhook event name. |
| `target` | body | `string` | yes | Webhook target URL. |
