# List Domains by Email Address with Host.io

Finds domains in Host.io by email address.

## Endpoint

- **Method:** `GET`
- **Path:** `/domains/email/:value`
- **Base URL:** `https://host.io/api`
- **Official documentation:** [List Domains by Email Address](https://host.io/docs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `value` | path | `string` | yes | Email address to search domains by. |
