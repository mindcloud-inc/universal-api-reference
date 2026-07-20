# List Swiss Communes by Canton with OpenPLZ

## Endpoint

- **Method:** `GET`
- **Path:** `/ch/Cantons/{key}/Communes`
- **Base URL:** `https://openplzapi.org`
- **Official documentation:** [List Swiss Communes by Canton](https://www.openplzapi.org/en/switzerland/#requesting-communes)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | path | `string` | yes | Swiss canton key. |
