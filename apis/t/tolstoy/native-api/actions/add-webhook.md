# Add Webhook with Tolstoy

Creates a new webhook in Tolstoy.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks/`
- **Base URL:** `https://api.gotolstoy.com`
- **Official documentation:** [Add Webhook](https://developers.gotolstoy.com/webhooks/add-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event` | body | `string` | yes | The event you want to subscribe to |
| `url` | body | `string` | yes | The url to send the event to |
