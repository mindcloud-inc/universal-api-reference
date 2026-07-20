# Unsubscribe Webhook with Rowform

Deletes a webhook subscription from Rowform.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/zapier/hooks`
- **Base URL:** `https://app.rowform.io`
- **Official documentation:** [Unsubscribe Webhook](https://help.rowform.io/api-reference#unsubscribe-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | yes | The webhook subscription id to remove. |
