# Get All Contacts with Alto

Retrieves all contact records from your Alto account.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts/all`
- **Base URL:** `https://api.alto.zoopladev.co.uk`
- **Official documentation:** [Get All Contacts](https://developers.vebraalto.com/api)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `active` | query | `boolean` | no | Whether to return active contacts. |
| `category` | query | `string` | no | Contact category filter. |
| `persona` | query | `string` | no | Contact persona filter. |
