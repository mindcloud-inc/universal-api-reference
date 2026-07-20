# Find Items By Tag with Priority Matrix

Finds Priority Matrix items by tag.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/item/`
- **Base URL:** `https://sync.appfluence.com`
- **Official documentation:** [Find Items By Tag](https://sync.appfluence.com/developer/guide/#common-api)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tag__name` | query | `string` | yes | Tag name to match. |
