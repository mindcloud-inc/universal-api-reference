# List Partners with BoxHero

Retrieves partners from BoxHero.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/partners`
- **Base URL:** `https://rest.boxhero-app.com`
- **Official documentation:** [List Partners](https://rest.boxhero-app.com/docs/api#/partners/VendorsController_getVendors)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cursor` | query | `number` | no | Cursor for the next page of partners |
| `limit` | query | `number` | no | Maximum number of partners to return |
| `type` | query | `number` | no | Filter partners by type: supplier or customer |
