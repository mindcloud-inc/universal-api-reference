# Delete Webhook with Placker

## Endpoint

- **Method:** `DELETE`
- **Path:** `/webhook/:board/:webhook`
- **Base URL:** `https://api.placker.com`
- **Official documentation:** [Delete Webhook](https://placker.com/docs/api/paths/webhook.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `board` | path | `number` | yes | Board ID. |
| `webhook` | path | `string` | yes | Webhook ID. |
