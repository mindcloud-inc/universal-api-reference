# List Companies with Assembly.com

Retrieves companies from Assembly.com.

## Endpoint

- **Method:** `GET`
- **Path:** `/companies`
- **Base URL:** `https://api.assembly.com/v1`
- **Official documentation:** [List Companies](https://docs.assembly.com/reference/list-companies)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | The name of the company to query for. |
| `isPlaceholder` | query | `boolean` | no | If true, filter for all placeholder companies. |
