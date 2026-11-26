# eBay: Create Inventory Location

Create a new Inventory Location.

```
POST https://connect.mindcloud.co/v1/universal/ebay/latest/actions/create-inventory-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eBay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ebay/latest/actions/create-inventory-location" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "merchantLocationKey": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ebay/latest/actions/create-inventory-location', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "merchantLocationKey": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `location.address` | object | no |  |
| `location.address.addressLine1` | string | no | The first line of a street address. This field is required for store and fulfillment center locations. A street address is not required for warehouse locations. |
| `location.geoCoordinates.latitude` | string | no | The latitude (North-South) component of the geographic coordinate. This field is required if a geoCoordinates container is used. This field is returned if geographical coordinates are set for the location. Example: 33.089805 |
| `locationTypes` | list<string> | no | Define the function of this inventory location. Typically, an inventory location will serve as a store, warehouse, or fulfillment center, but in some cases, an inventory location may be more than one type. Accepts multiple values as an array. |
| `merchantLocationKey` | string | yes | This specifies the unique, seller-defined key (ID) for an inventory location. Max length: 36 (characters). No spaces, but you may use a dash '-' or underscore '_'. |
| `location.address.addressLine2` | string | no | The second line of a street address. This field can be used for additional address information, such as a suite or apartment number. This field will be returned if defined for an inventory location. |
| `location.geoCoordinates` | object | no | This container is used to set the Global Positioning System (GPS) latitude and longitude coordinates for the inventory location. Geographical coordinates are required for the location of In-Store Pickup inventory. |
| `location.geoCoordinates.longitude` | string | no | The longitude (East-West) component of the geographic coordinate. This field is required if a geoCoordinates container is used. This field is returned if geographical coordinates are set for the location. Example: -88.709822 |
| `name` | string | no | The seller-defined name of the inventory location. This name should be a human-friendly name as it will be displayed in In-Store Pickup and Click and Collect listings. A name is not required for warehouse locations. For store locations, this field is not immediately required, but will be required before an offer enabled with the In-Store Pickup or Click and Collect capability can be published. |
| `location.address.city` | string | no | The city in which the inventory location resides. This field is required for store and fulfillment center locations. For warehouse locations, this field is conditionally required as part of a city and stateOrProvince pair if a postalCode is not provided. If a postalCode is provided, the city is derived from the provided postal code and this field is technically optional. |
| `merchantLocationStatus` | list | no | Indicate whether the inventory location will be created with the status: ENABLED (inventory can be loaded to location) or DISABLED (inventory can not be loaded to location). If this field is omitted, a successful request will automatically enable the location. |
| `location.address.stateOrProvince` | string | no | The state/province in which the inventory location resides. This field is required for store and fulfillment center locations. For warehouse locations, this field is conditionally required as part of a city and stateOrProvince pair if a postalCode is not provided. If a postalCode is provided, the state or province is derived from the provided zip code and this field is technically optional. |
| `locationWebUrl` | string | no | This text field is used by the merchant to provide the Website address (URL) associated with the inventory location. |
| `location` | object | no |  |
| `location.address.postalCode` | string | no | The postal/zip code of the address. eBay uses postal codes to surface In-Store Pickup items within the vicinity of a buyer's location, and it also uses postal codes (origin and destination) to estimate shipping costs when the seller uses calculated shipping. This field is required for store and fulfillment center locations. For warehouse locations, this field is conditionally required if a city and stateOrProvince pair is not provided. Note: For warehouse locations, city and stateOrProvince pair can be used instead of a postalCode value, and then the postal code is automatically derived from the city and state/province. |
| `location.address.county` | string | no | The county in which the address resides. (optional) |
| `location.address.country` | string | no | The country in which the address resides, represented as two-letter ISO 3166 country code. For example, US represents the United States, and DE represents Germany. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native eBay API, this operation is `POST sell/inventory/v1/location/:merchantLocationKey` (base URL `https://api.ebay.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-inventory-location.md) for the provider-specific parameters and requirements.

