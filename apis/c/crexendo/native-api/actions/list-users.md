# List Users with Crexendo

Retrieves users for a domain in Crexendo.

## Endpoint

- **Method:** `GET`
- **Path:** `/domains/:domain/users`
- **Base URL:** `https://ns-api.com/ns-api/v2`
- **Official documentation:** [List Users](https://docs.ns-api.com/reference/getusers)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | path | `string` | yes | Domain identifier, for example apps.mindcloud.co. |
