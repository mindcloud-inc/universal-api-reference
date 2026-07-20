# Create Appointment with Néctar CRM

Creates a new appointment in Néctar CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/compromissos/`
- **Base URL:** `https://app.nectarcrm.com.br/crm/api/1`
- **Official documentation:** [Create Appointment](https://nectarcrm.docs.apiary.io/#reference/0/compromissos/criar)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assunto` | body | `string` | yes | Appointment subject. |
| `dataInicio` | body | `date` | yes | Appointment start datetime. |
| `dataFim` | body | `date` | yes | Appointment end datetime. |
| `cliente` | body | `object` | yes | Contact object for the appointment, for example {"id": 2}. |
