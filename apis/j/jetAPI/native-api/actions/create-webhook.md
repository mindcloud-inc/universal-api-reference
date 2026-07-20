# Create Webhook with JetAPI

Creates a new webhook in JetAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/webhooks`
- **Base URL:** `https://api.jetapi.io`
- **Official documentation:** [Create Webhook](https://docs.jetapi.io/#1acdd39e-f338-4664-8aa9-07bd1b875556)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | The address to which the notification is sent. |
| `types[]` | query | `array<string>` | yes | List of webhook events. |
