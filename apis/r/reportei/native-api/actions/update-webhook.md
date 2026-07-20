# Update Webhook with Reportei

Updates an existing webhook in Reportei.

## Endpoint

- **Method:** `PUT`
- **Path:** `/webhooks/:id`
- **Base URL:** `https://app.reportei.com/api/v2`
- **Official documentation:** [Update Webhook](https://developers.reportei.com#webhooks-endpoint-4)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID do webhook. |
| `url` | body | `string` | no | URL de callback atualizada. |
| `event_type` | body | `string` | no | Tipo de evento atualizado. |
| `project_id` | body | `number` | no | ID do projeto. |
