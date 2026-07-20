# List Entity Statements with OpenSanctions

## Endpoint

- **Method:** `GET`
- **Path:** `/statements`
- **Base URL:** `https://api.opensanctions.org`
- **Official documentation:** [List Entity Statements](https://api.opensanctions.org/docs#/Data%20access/statements_statements_get)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entity_id` | query | `string` | no | Filter statements by source entity ID. |
