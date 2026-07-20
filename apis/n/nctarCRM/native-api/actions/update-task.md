# Update Task with Néctar CRM

Updates an existing task in Néctar CRM.

## Endpoint

- **Method:** `PUT`
- **Path:** `/tarefas/:id`
- **Base URL:** `https://app.nectarcrm.com.br/crm/api/1`
- **Official documentation:** [Update Task](https://nectarcrm.docs.apiary.io/#reference/0/tarefas/editar)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Task ID. |
| `titulo` | body | `string` | yes | Updated task title. |
