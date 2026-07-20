# List Agenda Records with GIRITON

Retrieves records from a specific GIRITON agenda.

## Endpoint

- **Method:** `GET`
- **Path:** `/agendas/:agendaId/records`
- **Base URL:** `https://rest.giriton.com/system/api`
- **Official documentation:** [List Agenda Records](https://rest.giriton.com/apidoc/#/Agenda/getRecords)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agendaId` | path | `string` | yes | Agenda ID. |
