# Update Contact with Néctar CRM

Updates an existing contact in Néctar CRM.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contatos/:id`
- **Base URL:** `https://app.nectarcrm.com.br/crm/api/1`
- **Official documentation:** [Update Contact](https://nectarcrm.docs.apiary.io/#reference/0/contatos/editar)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Contact ID. |
| `nome` | body | `string` | yes | Updated contact name. |
