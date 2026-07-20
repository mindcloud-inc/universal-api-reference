# List Calls with echowin

Retrieves calls from echowin.

## Endpoint

- **Method:** `GET`
- **Path:** `/calls`
- **Base URL:** `https://echo.win/api/v1`
- **Official documentation:** [List Calls](https://echo.win/api-docs/calls#list-calls)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `search` | query | `string` | no |
| `callType` | query | `string` | no |
| `agentId` | query | `string` | no |
| `minDuration` | query | `number` | no |
| `maxDuration` | query | `number` | no |
| `dateFrom` | query | `date` | no |
| `dateTo` | query | `date` | no |
