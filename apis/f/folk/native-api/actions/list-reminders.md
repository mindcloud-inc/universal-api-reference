# List Reminders with folk

Retrieves a list of reminders from folk.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/reminders`
- **Base URL:** `https://api.folk.app`
- **Official documentation:** [List Reminders](https://developer.folk.app/api-reference/reminders/list-reminders)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entity.id` | query | `string` | no | Filter reminders by entity. Only reminders linked to the specified entity will be returned. |
