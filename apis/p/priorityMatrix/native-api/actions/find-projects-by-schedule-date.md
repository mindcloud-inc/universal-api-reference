# Find Projects By Schedule Date with Priority Matrix

Finds Priority Matrix projects by schedule date.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/project/`
- **Base URL:** `https://sync.appfluence.com`
- **Official documentation:** [Find Projects By Schedule Date](https://sync.appfluence.com/developer/guide/#concrete-examples)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `startDate__gt` | query | `number` | yes | Start date lower bound as epoch seconds. |
