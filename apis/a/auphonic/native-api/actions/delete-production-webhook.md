# Delete Production Webhook with Auphonic

Deletes a production webhook from Auphonic.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/production/:uuid/webhook.json`
- **Base URL:** `https://auphonic.com/api`
- **Official documentation:** [Delete Production Webhook](https://auphonic.com/help/api/webhook.html#delete-a-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuid` | path | `string` | yes | UUID of the production. |
