# Update Webhook Field with AskHandle

Updates one AskHandle webhook field by UUID.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/webhooks/:uuid/`
- **Base URL:** `https://dashboard.askhandle.com/api/v1`
- **Official documentation:** [Update Webhook Field](https://dashboard.askhandle.com/api/v1/docs/api_reference.html#webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuid` | path | `string` | no | The webhook UUID. |
| `event` | body | `string` | yes | Webhook event name. |
| `target` | body | `string` | yes | Webhook target URL. |
