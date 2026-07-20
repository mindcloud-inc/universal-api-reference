# List Documents with GIRITON

Retrieves a list of documents from GIRITON.

## Endpoint

- **Method:** `GET`
- **Path:** `/documents`
- **Base URL:** `https://rest.giriton.com/system/api`
- **Official documentation:** [List Documents](https://rest.giriton.com/apidoc/#/Documents/getDocuments)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agendaId` | query | `string` | yes | Agenda ID to list documents for. |
