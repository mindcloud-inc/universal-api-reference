# List Bills with FreeAgent

Retrieves a list of bills from FreeAgent.

## Endpoint

- **Method:** `GET`
- **Path:** `/bills`
- **Base URL:** `https://api.freeagent.com/v2`
- **Official documentation:** [List Bills](https://dev.freeagent.com/docs/bills#list-all-bills)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact` | query | `string` | no | Filter bills by FreeAgent contact resource URL. |
| `project` | query | `string` | no | Filter bills by FreeAgent project resource URL. |
| `updated_since` | query | `date` | no | Only return bills updated after this timestamp. |
| `view` | query | `string` | no | Filter the bill collection by FreeAgent view. |
