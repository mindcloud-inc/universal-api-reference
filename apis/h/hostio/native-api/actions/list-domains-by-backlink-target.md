# List Domains by Backlink Target with Host.io

Finds domains in Host.io by backlink target.

## Endpoint

- **Method:** `GET`
- **Path:** `/domains/backlinks/:value`
- **Base URL:** `https://host.io/api`
- **Official documentation:** [List Domains by Backlink Target](https://host.io/docs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `value` | path | `string` | yes | Domain that result domains link to from their homepage. |
