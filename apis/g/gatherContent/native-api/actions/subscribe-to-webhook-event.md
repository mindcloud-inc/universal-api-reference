# Subscribe To Webhook Event with GatherContent

Subscribes a webhook to an event in GatherContent.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/webhooks/:event_name`
- **Base URL:** `https://api.gathercontent.com`
- **Official documentation:** [Subscribe To Webhook Event](https://docs.gathercontent.com/reference/subscribetowebhook-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event_name` | path | `string` | yes | Webhook event name. |
| `project_id` | path | `string` | yes | Project id. |
| `url` | body | `string` | yes | Webhook destination URL. |
