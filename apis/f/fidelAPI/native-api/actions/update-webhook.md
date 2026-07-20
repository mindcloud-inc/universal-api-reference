# Update Webhook with Fidel API

Updates an existing webhook in Fidel API.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/hooks/:hookId`
- **Base URL:** `https://api.fidel.uk/v1`
- **Official documentation:** [Update Webhook](https://reference.fidel.uk/reference/update-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hookId` | path | `string` | yes | — |
| `programId` | body | `string` | yes | The program ID. |
| `event` | body | `string` | yes | The webhook event. |
| `url` | body | `string` | yes | The destination URL. |
