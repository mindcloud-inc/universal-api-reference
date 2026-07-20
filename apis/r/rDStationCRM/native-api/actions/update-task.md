# Update Task with RD Station CRM

Updates an existing task in RD Station CRM.

## Endpoint

- **Method:** `PUT`
- **Path:** `/tasks/:id`
- **Base URL:** `https://api.rd.services/crm/v2`
- **Official documentation:** [Update Task](https://developers.rdstation.com/reference/crm-v2-update-task)

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
| `id` | path | `string` | yes | Task identifier. |
