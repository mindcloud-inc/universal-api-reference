# List Blacklist Entries with NobelSMS

Retrieves blacklist entries from NobelSMS.

## Endpoint

- **Method:** `GET`
- **Path:** `/black_list`
- **Base URL:** `https://api.nobelsms.com/rest`
- **Official documentation:** [List Blacklist Entries](https://api.nobelsms.com/rest/swagger.json)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bnumber` | query | `number` | no | B-number. |
| `tag_ids` | query | `string` | no | Comma-separated list of tag IDs. |
