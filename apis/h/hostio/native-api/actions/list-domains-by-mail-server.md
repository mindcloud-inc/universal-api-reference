# List Domains by Mail Server with Host.io

Finds domains in Host.io by mail server.

## Endpoint

- **Method:** `GET`
- **Path:** `/domains/mx/:value`
- **Base URL:** `https://host.io/api`
- **Official documentation:** [List Domains by Mail Server](https://host.io/docs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `value` | path | `string` | yes | Root domain of the mail server to search by. |
