# List Domains by Redirect Target with Host.io

Finds domains in Host.io by redirect target.

## Endpoint

- **Method:** `GET`
- **Path:** `/domains/redirects/:value`
- **Base URL:** `https://host.io/api`
- **Official documentation:** [List Domains by Redirect Target](https://host.io/docs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `value` | path | `string` | yes | Domain that result domains redirect to from their homepage. |
