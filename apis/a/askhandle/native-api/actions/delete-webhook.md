# Delete Webhook with AskHandle

Deletes an existing AskHandle webhook by UUID.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/webhooks/:uuid/`
- **Base URL:** `https://dashboard.askhandle.com/api/v1`
- **Official documentation:** [Delete Webhook](https://dashboard.askhandle.com/api/v1/docs/api_reference.html#webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuid` | path | `string` | no | The webhook UUID. |
