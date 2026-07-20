# Create Webhook with Locu

Creates a new webhook in Locu.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks`
- **Base URL:** `https://api.locu.app/api/v1`
- **Official documentation:** [Create Webhook](https://locu.app/api/docs#tag/webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Webhook destination URL. |
