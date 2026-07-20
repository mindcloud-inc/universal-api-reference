# Get Process Impact Process Item with Grand Avenue Software

Retrieves a process impact's related process item from Grand Avenue Software.

## Endpoint

- **Method:** `GET`
- **Path:** `/ProcessImpacts/:id/ProcessItem`
- **Base URL:** `{baseUrl}`
- **API:** REST

## Capabilities

This operation supports [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$select` | query | `list<string>` | no | Send multiple values as a string. |
| `id` | path | `string` | yes | — |
