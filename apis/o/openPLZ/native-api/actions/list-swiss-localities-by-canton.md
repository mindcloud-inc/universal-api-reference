# List Swiss Localities by Canton with OpenPLZ

## Endpoint

- **Method:** `GET`
- **Path:** `/ch/Cantons/{key}/Localities`
- **Base URL:** `https://openplzapi.org`
- **Official documentation:** [List Swiss Localities by Canton](https://www.openplzapi.org/en/switzerland/#requesting-postal-codes-and-localities)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | path | `string` | yes | Swiss canton key. |
