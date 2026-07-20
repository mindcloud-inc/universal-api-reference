# Create Shipment with TrackMage

Creates a new shipment in TrackMage.

## Endpoint

- **Method:** `POST`
- **Path:** `/shipments`
- **Base URL:** `https://api.trackmage.com/`
- **Official documentation:** [Create Shipment](https://docs.trackmage.com/docs/shipment/shipment.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `trackingNumber` | body | `string` | no | A tracking number, provided by the shipping company. |
| `orderNumbers[]` | body | `array<string>` | no | List of order numbers to which the shipment belongs. |
| `email` | body | `string` | no | Customer email address. |
| `phoneNumber` | body | `string` | no | Customer phone number. |
| `originCarrier` | body | `string` | no | The code of origin [carrier](https://trackmage.com/carriers/). Origin Carrier will be identified automatically based on Tracking Number. Sometimes the carrier cannot be identified. In that case, the system will return the error with the suggested carriers list in the payload. The value of this field can be specified only once in POST request. |
| `workspace` | body | `string` | yes | The workspace reference to which the shipment belongs. |
| `orders[]` | body | `array<string>` | no | List of order references to which the shipment belongs. |
| `shipmentItems[]` | body | `array<object>` | no | List of shipment items references that belong to the shipment. |
| `externalSourceIntegration` | body | `string` | no | The workflow reference to integration for ecommerce store. |
| `externalSourceSyncId` | body | `string` | no | The id of the shipment in ecommerce store (WooCommerce, Shopify, etc.). |
| `fulfillmentIntegration` | body | `string` | no | The workflow reference to integration for fulfillment source. |
| `fulfillmentSyncId` | body | `string` | no | The id of the shipment in the fulfillment source system (AliExpress, Amazon, etc.). |
| `address.addressLine1` | body | `string` | no | The street address. This field is optional. |
| `address.addressLine2` | body | `string` | no | An optional additional field for the street address. This field is optional. |
| `address.city` | body | `string` | no | The city, town, or village. This field is optional. |
| `address.company` | body | `string` | no | The company of the person associated with the address. This field is optional. |
| `address.country` | body | `string` | no | The name of the country. This field is optional. |
| `address.countryIso2` | body | `string` | no | The two-letter country code. This field is optional. |
| `address.firstName` | body | `string` | no | The first name of the person associated with the address. This field is optional. |
| `address.lastName` | body | `string` | no | The last name of the person associated with the address. This field is optional. |
| `address.postcode` | body | `string` | no | The postal code (zip, postcode, Eircode, …). This field is optional. |
| `address.state` | body | `string` | no | The name of the region (province, state, prefecture, …). This field is optional. |
| `shipmentStatus.code` | body | `string` | no | A unique status code. This field is required. |
| `shipmentStatus.title` | body | `string` | no | A status name. This field is optional. |
| `shipmentStatus.description` | body | `string` | no | — |
