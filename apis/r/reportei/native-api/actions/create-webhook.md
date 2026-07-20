# Create Webhook with Reportei

Creates a new webhook in Reportei.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks`
- **Base URL:** `https://app.reportei.com/api/v2`
- **Official documentation:** [Create Webhook](https://developers.reportei.com#webhooks-endpoint-3)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | URL de callback para receber os eventos. |
| `event_type` | body | `string` | yes | Tipo de evento a monitorar. |
| `project_id` | body | `number` | no | ID do projeto para filtrar eventos. |
