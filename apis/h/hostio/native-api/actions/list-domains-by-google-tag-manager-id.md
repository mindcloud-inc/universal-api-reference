# List Domains by Google Tag Manager ID with Host.io

Finds domains in Host.io by Google Tag Manager ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/domains/gtm/:value`
- **Base URL:** `https://host.io/api`
- **Official documentation:** [List Domains by Google Tag Manager ID](https://host.io/docs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `value` | path | `string` | yes | Google Tag Manager ID to search domains by. |
