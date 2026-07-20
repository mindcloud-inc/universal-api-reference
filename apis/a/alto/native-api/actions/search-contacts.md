# Search Contacts with Alto

Finds contacts in Alto by search criteria.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts/search`
- **Base URL:** `https://api.alto.zoopladev.co.uk`
- **Official documentation:** [Search Contacts](https://developers.vebraalto.com/api)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact-type` | query | `string` | no | Contact type filter. |
| `query` | query | `string` | yes | Search text for contacts. |
| `archived` | query | `boolean` | no | Whether to search archived contacts. |
