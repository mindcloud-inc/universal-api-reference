# List Call Queues with Crexendo

Retrieves call queues for a domain in Crexendo.

## Endpoint

- **Method:** `GET`
- **Path:** `/domains/:domain/callqueues`
- **Base URL:** `https://ns-api.com/ns-api/v2`
- **Official documentation:** [List Call Queues](https://docs.ns-api.com/reference/readcallqueues)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | path | `string` | yes | Domain identifier, for example apps.mindcloud.co. |
