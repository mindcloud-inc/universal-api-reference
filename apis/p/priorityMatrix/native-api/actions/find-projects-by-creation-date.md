# Find Projects By Creation Date with Priority Matrix

Finds Priority Matrix projects by creation date.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/project/`
- **Base URL:** `https://sync.appfluence.com`
- **Official documentation:** [Find Projects By Creation Date](https://sync.appfluence.com/developer/guide/#concrete-examples)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `creationDate__gt` | query | `number` | yes | Creation date lower bound as epoch seconds. |
