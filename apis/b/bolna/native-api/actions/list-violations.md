# List Violations with Bolna

Retrieves violations for your Bolna account.

## Endpoint

- **Method:** `GET`
- **Path:** `/violations/list`
- **Base URL:** `https://api.bolna.ai`
- **Official documentation:** [List Violations](https://www.bolna.ai/docs/api-reference/violations/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `string` | no | Optional violation status filter. |
