# Create Task with Néctar CRM

Creates a new task in Néctar CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/tarefas/`
- **Base URL:** `https://app.nectarcrm.com.br/crm/api/1`
- **Official documentation:** [Create Task](https://nectarcrm.docs.apiary.io/#reference/0/tarefas/criar)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `titulo` | body | `string` | yes | Task title. |
| `dataLimite` | body | `date` | yes | Task due date as an ISO 8601 datetime. |
| `cliente` | body | `object` | yes | Contact object for the task, for example {"id": 2}. |
| `descricao` | body | `string` | no | Task description. |
