# List Contacts with NobelSMS

Retrieves contacts from NobelSMS.

## Endpoint

- **Method:** `GET`
- **Path:** `/contact`
- **Base URL:** `https://api.nobelsms.com/rest`
- **Official documentation:** [List Contacts](https://api.nobelsms.com/rest/swagger.json)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `blacklisted` | query | `number` | no | Blacklist flag. |
| `first_name` | query | `string` | no | First name. |
| `last_name` | query | `string` | no | Last name. |
| `phone` | query | `string` | no | Phone number. |
| `tag_ids` | query | `string` | no | Comma-separated list of tag IDs. |
