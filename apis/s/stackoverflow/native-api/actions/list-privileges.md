# List Privileges with Stackoverflow

Retrieves site privileges from Stackoverflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/privileges`
- **Base URL:** `https://api.stackexchange.com/2.3`
- **Official documentation:** [List Privileges](https://api.stackexchange.com/docs/privileges)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `site` | query | `string` | yes | API site parameter, for example stackoverflow. |
