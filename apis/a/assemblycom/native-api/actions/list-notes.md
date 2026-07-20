# List Notes with Assembly.com

Retrieves notes from Assembly.com.

## Endpoint

- **Method:** `GET`
- **Path:** `/notes`
- **Base URL:** `https://api.assembly.com/v1`
- **Official documentation:** [List Notes](https://docs.assembly.com/reference/list-notes)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entityId` | query | `string` | no | Only return notes for the entity specified by this ID. |
| `entityType` | query | `string` | no | Only return notes that have an entity type matching this value. |
