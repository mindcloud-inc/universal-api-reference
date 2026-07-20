# List Estimates with FreeAgent

Retrieves a list of estimates from FreeAgent.

## Endpoint

- **Method:** `GET`
- **Path:** `/estimates`
- **Base URL:** `https://api.freeagent.com/v2`
- **Official documentation:** [List Estimates](https://dev.freeagent.com/docs/estimates#list-all-estimates)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact` | query | `string` | no | Filter estimates by FreeAgent contact resource URL. |
| `invoice` | query | `string` | no | Filter estimates by FreeAgent invoice resource URL. |
| `project` | query | `string` | no | Filter estimates by FreeAgent project resource URL. |
| `updated_since` | query | `date` | no | Only return estimates updated after this timestamp. |
| `view` | query | `string` | no | Filter the estimate collection by FreeAgent view. |
