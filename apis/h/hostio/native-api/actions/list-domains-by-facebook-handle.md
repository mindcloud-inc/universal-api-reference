# List Domains by Facebook Handle with Host.io

Finds domains in Host.io by Facebook handle.

## Endpoint

- **Method:** `GET`
- **Path:** `/domains/facebook/:value`
- **Base URL:** `https://host.io/api`
- **Official documentation:** [List Domains by Facebook Handle](https://host.io/docs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `value` | path | `string` | yes | Facebook handle to search for. |
