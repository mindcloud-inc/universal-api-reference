# List Schemas with Rossum

Retrieves schemas from Rossum.

## Endpoint

- **Method:** `GET`
- **Path:** `/schemas`
- **Base URL:** `https://mindcloud.rossum.app/api/v1`
- **Official documentation:** [List Schemas](https://rossum.app/api/docs/openapi/)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | no | Filter schemas by ID. |
| `name` | query | `string` | no | Filter schemas by name. |
| `ordering` | query | `string` | no | Sort schemas by a supported Rossum ordering value. |
| `queue` | query | `string` | no | Filter schemas by queue ID. |
