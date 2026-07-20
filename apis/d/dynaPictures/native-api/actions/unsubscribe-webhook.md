# Unsubscribe Webhook with DynaPictures

Deletes a webhook subscription from DynaPictures.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/hooks`
- **Base URL:** `https://api.dynapictures.com`
- **Official documentation:** [Unsubscribe Webhook](https://dynapictures.com/docs/#unsubscribe-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `targetUrl` | body | `string` | yes | Webhook URL that receives notifications. |
| `templateId` | body | `string` | yes | UID of the template to stop watching. |
