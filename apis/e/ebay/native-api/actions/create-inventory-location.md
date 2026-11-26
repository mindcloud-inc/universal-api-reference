# Create Inventory Location with eBay

Create a new Inventory Location.

## Endpoint

- **Method:** `POST`
- **Path:** `sell/inventory/v1/location/:merchantLocationKey`
- **Base URL:** `https://api.ebay.com/`
- **API:** REST
- **Official documentation:** [Create Inventory Location](https://developer.ebay.com/api-docs/sell/inventory/resources/location/methods/createInventoryLocation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `location.address` | body | `object` | no | — |
| `location.address.addressLine1` | body | `string` | no | The first line of a street address. This field is required for store and fulfillment center locations. A street address is not required for warehouse locations. |
| `location.geoCoordinates.latitude` | body | `string` | no | The latitude (North-South) component of the geographic coordinate. This field is required if a geoCoordinates container is used.  This field is returned if geographical coordinates are set for the location.  Example: 33.089805 |
| `locationTypes` | body | `list<string>` | no | Define the function of this inventory location. Typically, an inventory location will serve as a store, warehouse, or fulfillment center, but in some cases, an inventory location may be more than one type. Send multiple values as a array. |
| `merchantLocationKey` | path | `string` | yes | This specifies the unique, seller-defined key (ID) for an inventory location. Max length: 36 (characters). No spaces, but you may use a dash '-' or underscore '_'. Maximum length: 36. |
| `location.address.addressLine2` | body | `string` | no | The second line of a street address. This field can be used for additional address information, such as a suite or apartment number.  This field will be returned if defined for an inventory location. |
| `location.geoCoordinates` | body | `object` | no | This container is used to set the Global Positioning System (GPS) latitude and longitude coordinates for the inventory location.  Geographical coordinates are required for the location of In-Store Pickup inventory. |
| `location.geoCoordinates.longitude` | body | `string` | no | The longitude (East-West) component of the geographic coordinate. This field is required if a geoCoordinates container is used.  This field is returned if geographical coordinates are set for the location.  Example: -88.709822 |
| `name` | body | `string` | no | The seller-defined name of the inventory location. This name should be a human-friendly name as it will be displayed in In-Store Pickup and Click and Collect listings. A name is not required for warehouse locations. For store locations, this field is not immediately required, but will be required before an offer enabled with the In-Store Pickup or Click and Collect capability can be published. |
| `location.address.city` | body | `string` | no | The city in which the inventory location resides. This field is required for store and fulfillment center locations. For warehouse locations, this field is conditionally required as part of a city and stateOrProvince pair if a postalCode is not provided. If a postalCode is provided, the city is derived from the provided postal code and this field is technically optional. |
| `merchantLocationStatus` | body | `list` | no | Indicate whether the inventory location will be created with the status: ENABLED (inventory can be loaded to location) or DISABLED (inventory can not be loaded to location). If this field is omitted, a successful request will automatically enable the location. |
| `location.address.stateOrProvince` | body | `string` | no | The state/province in which the inventory location resides. This field is required for store and fulfillment center locations. For warehouse locations, this field is conditionally required as part of a city and stateOrProvince pair if a postalCode is not provided. If a postalCode is provided, the state or province is derived from the provided zip code and this field is technically optional. |
| `locationWebUrl` | body | `string` | no | This text field is used by the merchant to provide the Website address (URL) associated with the inventory location. |
| `location` | body | `object` | no | — |
| `location.address.postalCode` | body | `string` | no | The postal/zip code of the address. eBay uses postal codes to surface In-Store Pickup items within the vicinity of a buyer's location, and it also uses postal codes (origin and destination) to estimate shipping costs when the seller uses calculated shipping. This field is required for store and fulfillment center locations. For warehouse locations, this field is conditionally required if a city and stateOrProvince pair is not provided. Note: For warehouse locations, city and stateOrProvince pair can be used instead of a postalCode value, and then the postal code is automatically derived from the city and state/province. |
| `location.address.county` | body | `string` | no | The county in which the address resides. (optional) |
| `location.address.country` | body | `string` | no | The country in which the address resides, represented as two-letter ISO 3166 country code. For example, US represents the United States, and DE represents Germany. |
