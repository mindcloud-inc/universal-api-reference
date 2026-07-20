# List Domains by Twitter Handle with Host.io

Finds domains in Host.io by Twitter handle.

## Endpoint

- **Method:** `GET`
- **Path:** `/domains/twitter/:value`
- **Base URL:** `https://host.io/api`
- **Official documentation:** [List Domains by Twitter Handle](https://host.io/docs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `value` | path | `string` | yes | Twitter handle to search for. |
