# Update Appointment with Néctar CRM

Updates an existing appointment in Néctar CRM.

## Endpoint

- **Method:** `PUT`
- **Path:** `/compromissos/:id`
- **Base URL:** `https://app.nectarcrm.com.br/crm/api/1`
- **Official documentation:** [Update Appointment](https://nectarcrm.docs.apiary.io/#reference/0/compromissos/editar)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Appointment ID. |
| `assunto` | body | `string` | yes | Updated appointment subject. |
