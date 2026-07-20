# List Channel Items with JmpTo

Retrieves items from a channel in JmpTo.

## Endpoint

- **Method:** `GET`
- **Path:** `/channel/:id`
- **Base URL:** `https://jmpto.net/api`
- **Official documentation:** [List Channel Items](https://jmpto.net/developers#list-channel-items)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Channel ID whose items should be listed. |
