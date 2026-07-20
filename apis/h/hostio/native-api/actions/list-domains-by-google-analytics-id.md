# List Domains by Google Analytics ID with Host.io

Finds domains in Host.io by Google Analytics ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/domains/googleanalytics/:value`
- **Base URL:** `https://host.io/api`
- **Official documentation:** [List Domains by Google Analytics ID](https://host.io/docs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `value` | path | `string` | yes | Google Analytics ID to search domains by. |
