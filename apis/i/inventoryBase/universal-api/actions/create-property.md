# InventoryBase: Create Property

Creates a new property record in InventoryBase.

```
POST https://connect.mindcloud.co/v1/universal/inventoryBase/latest/actions/create-property
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InventoryBase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/inventoryBase/latest/actions/create-property" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "address": {},
  "noOfBeds": 1,
  "noOfBaths": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/inventoryBase/latest/actions/create-property', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "address": {},
    "noOfBeds": 1,
    "noOfBaths": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `address` | object | yes | The property's address object. |
| `noOfBeds` | number | yes | The number of bedrooms. |
| `noOfBaths` | number | yes | The number of bathrooms. |
| `noOfGarages` | number | no | The number of garages. |
| `parking` | boolean | no | Whether the property has parking. |
| `garden` | boolean | no | Whether the property has a garden. |
| `furnished` | string | no | The furnished status. |
| `type` | string | no | The property type. |
| `ref` | string | no | A user-defined property reference. |
| `notes` | string | no | Notes about the property. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "address": {
        "city": "string",
        "country": "string",
        "county": "string",
        "line1": "string",
        "line2": "string",
        "postcode": "string"
      },
      "areas": 1,
      "client": {},
      "customFields": {},
      "defaultClerk": {},
      "detachment": "string",
      "externalSize": 1,
      "furnished": "string",
      "garden": true,
      "geocoords": {
        "lat": 1,
        "lng": 1
      },
      "geocoordsOverridden": true,
      "hasElevator": true,
      "health": {},
      "id": 1,
      "image": {},
      "internalSize": 1,
      "noOfBaths": 1,
      "noOfBeds": 1,
      "noOfFloors": 1,
      "noOfGarages": 1,
      "noOfUnits": 1,
      "notes": "string",
      "parentPropertyId": 1,
      "parking": true,
      "propertyLinkedSchedules": [
        {}
      ],
      "propertyType": {
        "category": 1,
        "id": 1,
        "title": "string"
      },
      "ref": "string",
      "tags": [
        "string"
      ],
      "timezone": "string",
      "type": "string",
      "uprn": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `address` | object |  |
| `address.city` | string |  |
| `address.country` | string |  |
| `address.county` | string |  |
| `address.line1` | string |  |
| `address.line2` | string |  |
| `address.postcode` | string |  |
| `areas` | number |  |
| `client` | object |  |
| `customFields` | object |  |
| `defaultClerk` | object |  |
| `detachment` | string |  |
| `externalSize` | number |  |
| `furnished` | string |  |
| `garden` | boolean |  |
| `geocoords` | object |  |
| `geocoords.lat` | number |  |
| `geocoords.lng` | number |  |
| `geocoordsOverridden` | boolean |  |
| `hasElevator` | boolean |  |
| `health` | object |  |
| `id` | number |  |
| `image` | object |  |
| `internalSize` | number |  |
| `noOfBaths` | number |  |
| `noOfBeds` | number |  |
| `noOfFloors` | number |  |
| `noOfGarages` | number |  |
| `noOfUnits` | number |  |
| `notes` | string |  |
| `parentPropertyId` | number |  |
| `parking` | boolean |  |
| `propertyLinkedSchedules` | array<object> |  |
| `propertyType` | object |  |
| `propertyType.category` | number |  |
| `propertyType.id` | number |  |
| `propertyType.title` | string |  |
| `ref` | string |  |
| `tags` | array<string> |  |
| `timezone` | string |  |
| `type` | string |  |
| `uprn` | string |  |

## Native endpoint

Through the native InventoryBase API, this operation is `POST /properties` (base URL `https://api.inventorybase.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-property.md) for the provider-specific parameters and requirements.

