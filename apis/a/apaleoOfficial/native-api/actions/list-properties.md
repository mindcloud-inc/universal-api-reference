# List Properties with Apaleo Official

Retrieves properties from your Apaleo Official account.

## Endpoint

- **Method:** `GET`
- **Path:** `/inventory/v1/properties`
- **Base URL:** `https://api.apaleo.com`
- **Official documentation:** [List Properties](https://api.apaleo.com/swagger/index.html?urls.primaryName=Inventory%20V1#/Property/InventoryPropertiesGet)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status[]` | query | `array<string>` | no | Filter properties by lifecycle status. |
| `includeArchived` | query | `boolean` | no | Include archived properties in the result set. |
| `countryCode[]` | query | `array<string>` | no | Filter properties by ISO country code. |
| `expand[]` | query | `array<string>` | no | Expand related nested resources in the response. |
