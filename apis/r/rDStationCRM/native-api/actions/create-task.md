# Create Task with RD Station CRM

Creates a new task in RD Station CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks`
- **Base URL:** `https://api.rd.services/crm/v2`
- **Official documentation:** [Create Task](https://developers.rdstation.com/reference/crm-v2-create-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | yes | Task payload documented in endpoint reference. |
| `data.completed_by_id` | body | `string` | no | ID do usuário que concluiu a tarefa. |
| `data.created_by_id` | body | `string` | no | ID do usuário que criou a tarefa. |
| `data.deal_id` | body | `string` | no | ID da negociação associada. |
| `data.description` | body | `string` | no | Notas ou descrição adicional da tarefa. |
| `data.due_date` | body | `date` | no | Data limite para conclusão da tarefa. |
| `data.name` | body | `string` | no | Assunto da tarefa. |
| `data.owner_ids[]` | body | `array<string>` | no | IDs dos usuários responsáveis pela tarefa. |
| `data.status` | body | `string` | no | Status da tarefa. |
| `data.type` | body | `string` | no | Tipo da tarefa. |
