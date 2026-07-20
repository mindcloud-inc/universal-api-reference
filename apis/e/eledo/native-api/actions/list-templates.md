# List Templates with Eledo

Retrieves a list of templates from Eledo.

## Endpoint

- **Method:** `GET`
- **Path:** `/List`
- **Base URL:** `https://eledo.online/api/RESTv1`
- **Official documentation:** [List Templates](https://eledo.online/documentation/api_reference/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scope` | query | `string` | no | Use Mine or Public to choose template scope. |
| `limit` | query | `number` | no | — |
| `page` | query | `number` | no | — |
