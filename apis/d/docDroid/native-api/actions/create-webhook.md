# Create Webhook with DocDroid

Creates a new webhook in DocDroid.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhook`
- **Base URL:** `https://www.docdroid.com/api`
- **Official documentation:** [Create Webhook](https://www.docdroid.com/apidocs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event` | body | `list` | yes | The DocDroid event to subscribe to. Accepted values: `document.created`, `document.deleted`, `document.updated`, `document.uploaded`. |
| `target_url` | body | `string` | yes | The target URL for the webhook. |
