# Update Timeline Event with Reportei

Updates an existing timeline event in Reportei.

## Endpoint

- **Method:** `PUT`
- **Path:** `/timeline-events/:id`
- **Base URL:** `https://app.reportei.com/api/v2`
- **Official documentation:** [Update Timeline Event](https://developers.reportei.com#timeline-endpoint-3)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID do evento. |
| `project_id` | body | `number` | yes | ID do projeto. |
| `report_id` | body | `number` | no | ID do relatório. |
| `title` | body | `string` | yes | Título do evento. |
| `content` | body | `string` | yes | Conteúdo do evento. |
