# Find Projects By Tag with Priority Matrix

Finds Priority Matrix projects by tag.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/project/`
- **Base URL:** `https://sync.appfluence.com`
- **Official documentation:** [Find Projects By Tag](https://sync.appfluence.com/developer/guide/#common-api)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tag__name` | query | `string` | yes | Project tag name. |
