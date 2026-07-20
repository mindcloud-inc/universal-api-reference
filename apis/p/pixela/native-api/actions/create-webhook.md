# Create Webhook with Pixela

Creates a new webhook in Pixela.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/users/:username/webhooks`
- **Base URL:** `https://pixe.la`
- **Official documentation:** [Create Webhook](https://docs.pixe.la/entry/post-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `username` | path | `string` | yes | Pixela username in the request path. |
| `graphID` | body | `string` | yes | Target graph ID for the webhook. |
| `type` | body | `string` | yes | Webhook behavior: increment, decrement, add, subtract, or stopwatch. |
