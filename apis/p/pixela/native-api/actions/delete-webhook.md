# Delete Webhook with Pixela

Deletes an existing webhook from Pixela.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/users/:username/webhooks/:webhookHash`
- **Base URL:** `https://pixe.la`
- **Official documentation:** [Delete Webhook](https://docs.pixe.la/entry/delete-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `username` | path | `string` | yes | Pixela username in the request path. |
| `webhookHash` | path | `string` | yes | Pixela webhook hash to delete. |
