# Update Webhook with AskHandle

Updates an existing AskHandle webhook by UUID.

## Endpoint

- **Method:** `PUT`
- **Path:** `/webhooks/:uuid/`
- **Base URL:** `https://dashboard.askhandle.com/api/v1`
- **Official documentation:** [Update Webhook](https://dashboard.askhandle.com/api/v1/docs/api_reference.html#webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuid` | path | `string` | no | The webhook UUID. |
| `event` | body | `string` | yes | Webhook event name. |
| `target` | body | `string` | yes | Webhook target URL. |
