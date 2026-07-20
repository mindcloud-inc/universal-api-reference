# List Content By User with Pling

Retrieves public content from Pling by username.

## Endpoint

- **Method:** `GET`
- **Path:** `/content/data`
- **Base URL:** `https://api.pling.com/ocs/v1`
- **Official documentation:** [List Content By User](https://www.opendesktop.org/ocs-api)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user` | query | `string` | yes | Pling username whose content should be listed. |
