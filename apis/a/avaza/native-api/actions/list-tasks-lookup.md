# List Tasks Lookup with Avaza

Retrieves tasks lookup entries from Avaza.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/Task/Lookup`
- **Base URL:** `https://api.avaza.com`
- **Official documentation:** [List Tasks Lookup](https://api.avaza.com/#!/Task/TaskLookup)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectID` | query | `number` | yes | (required) The ProjectID to use when filtering Tasks |
| `hideCompleted` | query | `boolean` | no | (optional) true/false to hide completed tasks. Defaults false |
| `search` | query | `string` | no | (optional) Search string to match against Task title. Performs begins-with match |
