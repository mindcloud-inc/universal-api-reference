# Find Items By Date with Priority Matrix

Finds Priority Matrix items by creation date.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/item/`
- **Base URL:** `https://sync.appfluence.com`
- **Official documentation:** [Find Items By Date](https://sync.appfluence.com/developer/guide/#concrete-examples)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `creationDate__gt` | query | `number` | yes | Return items created after this Unix timestamp. |
