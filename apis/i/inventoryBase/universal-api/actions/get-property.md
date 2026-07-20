# InventoryBase: Get Property

Retrieves a property record from InventoryBase by ID.

```
GET https://connect.mindcloud.co/v1/universal/inventoryBase/latest/actions/get-property
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InventoryBase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/inventoryBase/latest/actions/get-property?connectionId=$CONNECTION_ID&propertyId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "propertyId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/inventoryBase/latest/actions/get-property?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `propertyId` | number | yes | The InventoryBase property ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {
        "city": "string",
        "country": "string",
        "line1": "string",
        "postcode": "string"
      },
      "areas": 1,
      "customFields": {},
      "furnished": "string",
      "garden": true,
      "geocoords": {
        "lat": 1,
        "lng": 1
      },
      "hasElevator": true,
      "id": 1,
      "noOfBaths": 1,
      "noOfBeds": 1,
      "noOfFloors": 1,
      "noOfGarages": 1,
      "noOfUnits": 1,
      "parking": true,
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
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | object |  |
| `address.city` | string |  |
| `address.country` | string |  |
| `address.line1` | string |  |
| `address.postcode` | string |  |
| `areas` | number |  |
| `customFields` | object |  |
| `furnished` | string |  |
| `garden` | boolean |  |
| `geocoords` | object |  |
| `geocoords.lat` | number |  |
| `geocoords.lng` | number |  |
| `hasElevator` | boolean |  |
| `id` | number |  |
| `noOfBaths` | number |  |
| `noOfBeds` | number |  |
| `noOfFloors` | number |  |
| `noOfGarages` | number |  |
| `noOfUnits` | number |  |
| `parking` | boolean |  |
| `propertyType` | object |  |
| `propertyType.category` | number |  |
| `propertyType.id` | number |  |
| `propertyType.title` | string |  |
| `ref` | string |  |
| `tags` | array<string> |  |
| `timezone` | string |  |
| `type` | string |  |

## Native endpoint

Through the native InventoryBase API, this operation is `GET /properties/:propertyId` (base URL `https://api.inventorybase.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-property.md) for the provider-specific parameters and requirements.

