# Subscribe Webhook with DynaPictures

Creates a webhook subscription in DynaPictures.

## Endpoint

- **Method:** `POST`
- **Path:** `/hooks`
- **Base URL:** `https://api.dynapictures.com`
- **Official documentation:** [Subscribe Webhook](https://dynapictures.com/docs/#subscribe-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `targetUrl` | body | `string` | yes | Webhook URL that will receive notifications. |
| `templateId` | body | `string` | yes | UID of the template to watch. |
