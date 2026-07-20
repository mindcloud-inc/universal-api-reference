# Get Training Record with Grand Avenue Software

Retrieves a training record from Grand Avenue Software by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/TrainingRecords/:id`
- **Base URL:** `{baseUrl}`
- **API:** REST

## Capabilities

This operation supports [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$select` | query | `list<string>` | no | Send multiple values as a string. |
| `$expand` | query | `list<string>` | no | Send multiple values as a string. |
| `id` | path | `string` | no | — |
