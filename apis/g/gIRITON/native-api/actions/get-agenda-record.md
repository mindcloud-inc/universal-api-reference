# Get Agenda Record with GIRITON

Retrieves a specific record from a GIRITON agenda.

## Endpoint

- **Method:** `GET`
- **Path:** `/agendas/:agendaId/records/:recordId`
- **Base URL:** `https://rest.giriton.com/system/api`
- **Official documentation:** [Get Agenda Record](https://rest.giriton.com/apidoc/#/Agenda/getRecord)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agendaId` | path | `string` | yes | Agenda ID. |
| `recordId` | path | `string` | yes | Agenda record ID. |
