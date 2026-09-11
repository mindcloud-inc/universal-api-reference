# Get All States By Country with BigCommerce

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/countries/:countryId/states`
- **Base URL:** `https://api.bigcommerce.com/stores/{storeHash}`

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `countryId` | path | `number` | no | — |
| `state_abbreviation` | query | `string` | no | Abbreviation for the state/province. |
| `state` | query | `string` | no | Name of the state/province. |
