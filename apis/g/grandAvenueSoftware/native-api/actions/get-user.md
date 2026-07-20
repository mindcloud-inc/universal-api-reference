# Get User with Grand Avenue Software

Retrieves a user from Grand Avenue Software by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/Users/:id`
- **Base URL:** `{baseUrl}`
- **API:** REST

## Capabilities

This operation supports [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `select` | query | `list<string>` | no | Send multiple values as a array. |
| `$expand` | query | `list<string>` | no | Send multiple values as a array. |
| `id` | path | `number` | yes | — |
