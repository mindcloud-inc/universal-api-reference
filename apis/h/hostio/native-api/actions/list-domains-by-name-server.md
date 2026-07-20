# List Domains by Name Server with Host.io

Finds domains in Host.io by name server.

## Endpoint

- **Method:** `GET`
- **Path:** `/domains/ns/:value`
- **Base URL:** `https://host.io/api`
- **Official documentation:** [List Domains by Name Server](https://host.io/docs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `value` | path | `string` | yes | Root domain of the name server to search by. |
