# List Content By Category with Pling

Retrieves public content from Pling by category.

## Endpoint

- **Method:** `GET`
- **Path:** `/content/data`
- **Base URL:** `https://api.pling.com/ocs/v1`
- **Official documentation:** [List Content By Category](https://www.opendesktop.org/ocs-api)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `categories` | query | `string` | yes | One or more Pling category IDs accepted by the OCS content endpoint. |
