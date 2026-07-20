# List Domains by IP Address with Host.io

Finds domains in Host.io by IP address.

## Endpoint

- **Method:** `GET`
- **Path:** `/domains/ip/:value`
- **Base URL:** `https://host.io/api`
- **Official documentation:** [List Domains by IP Address](https://host.io/docs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `value` | path | `string` | yes | IP address to search domains by. |
