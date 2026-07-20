# Get Owners with Alto

Retrieves owner records from your Alto account.

## Endpoint

- **Method:** `GET`
- **Path:** `/owners`
- **Base URL:** `https://api.alto.zoopladev.co.uk`
- **Official documentation:** [Get Owners](https://developers.vebraalto.com/api)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `active` | query | `boolean` | no | Whether to return active owners. |
| `contact-id` | query | `string` | no | Contact identifier filter. |
| `property-id` | query | `string` | no | Property identifier filter. |
