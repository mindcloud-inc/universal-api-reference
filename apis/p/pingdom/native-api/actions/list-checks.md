# List Checks with Pingdom

## Endpoint

- **Method:** `GET`
- **Path:** `/checks`
- **Base URL:** `https://api.pingdom.com/api/3.1`
- **Official documentation:** [List Checks](https://docs.pingdom.com/api/#tag/Checks)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `showencryption` | query | `boolean` | no | Include the encryption setting for each check. |
| `include_tags` | query | `boolean` | no | Include the tag list for each check. |
| `include_severity` | query | `boolean` | no | Include the severity level for each check. |
| `tags` | query | `string` | no | Comma-separated tag list used to filter returned checks. |
