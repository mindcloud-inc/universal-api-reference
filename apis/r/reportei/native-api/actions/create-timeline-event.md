# Create Timeline Event with Reportei

Creates a new timeline event in Reportei.

## Endpoint

- **Method:** `POST`
- **Path:** `/timeline-events`
- **Base URL:** `https://app.reportei.com/api/v2`
- **Official documentation:** [Create Timeline Event](https://developers.reportei.com#timeline-endpoint-2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | body | `number` | yes | ID do projeto. |
| `report_id` | body | `number` | no | ID do relatório. |
| `title` | body | `string` | yes | Título do evento. |
| `content` | body | `string` | yes | Conteúdo do evento. |
