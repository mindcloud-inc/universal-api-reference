# Get Equipment with Grand Avenue Software

Retrieves equipment from Grand Avenue Software by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/Equipment/:id`
- **Base URL:** `{baseUrl}`
- **API:** REST

## Capabilities

This operation supports [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | — |
| `$select` | query | `list<string>` | no | Send multiple values as a string. |
| `$expand` | query | `list<string>` | no | Send multiple values as a string. |
