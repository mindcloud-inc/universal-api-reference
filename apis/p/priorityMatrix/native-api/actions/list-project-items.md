# List Project Items with Priority Matrix

Retrieves items from a Priority Matrix project.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/project/:idd/items/`
- **Base URL:** `https://sync.appfluence.com`
- **Official documentation:** [List Project Items](https://sync.appfluence.com/developer/guide/#common-api)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idd` | path | `number` | yes | Project IDD. |
