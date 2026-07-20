# SOS Inventory: List Locations

Retrieves locations from SOS Inventory.

```
GET https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/list-locations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SOS Inventory `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/list-locations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/list-locations?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {
        "city": {},
        "country": {},
        "line1": {},
        "line2": {},
        "line3": {},
        "line4": {},
        "line5": {},
        "postalCode": {},
        "stateProvince": {}
      },
      "binTracking": true,
      "company": {},
      "contact": {},
      "defaultLocation": true,
      "email": {},
      "id": 1,
      "keys": {},
      "name": "Ava Chen",
      "nonNettable": true,
      "phone": {},
      "salesTaxRate": 1,
      "shippingTaxable": true,
      "syncToken": 1,
      "values": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address.city` | object |  |
| `address.country` | object |  |
| `address.line1` | object |  |
| `address.line2` | object |  |
| `address.line3` | object |  |
| `address.line4` | object |  |
| `address.line5` | object |  |
| `address.postalCode` | object |  |
| `address.stateProvince` | object |  |
| `binTracking` | boolean |  |
| `company` | object |  |
| `contact` | object |  |
| `defaultLocation` | boolean |  |
| `email` | object |  |
| `id` | number |  |
| `keys` | object |  |
| `name` | string |  |
| `nonNettable` | boolean |  |
| `phone` | object |  |
| `salesTaxRate` | number |  |
| `shippingTaxable` | boolean |  |
| `syncToken` | number |  |
| `values` | object |  |

## Native endpoint

Through the native SOS Inventory API, this operation is `GET /api/v2/location` (base URL `https://api.sosinventory.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-locations.md) for the provider-specific parameters and requirements.

