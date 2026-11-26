# eBay: List Inventory Locations

Retrieves all defined details for every inventory location associated with the authenticated seller's account.

```
GET https://connect.mindcloud.co/v1/universal/ebay/latest/actions/list-inventory-locations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eBay `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ebay/latest/actions/list-inventory-locations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ebay/latest/actions/list-inventory-locations?${params}`, {
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
      "fullAddress": "string",
      "location": {
        "address": {
          "city": "string",
          "country": "string",
          "postalCode": "string",
          "stateOrProvince": "string"
        },
        "locationId": "string"
      },
      "locationTypes": [
        "string"
      ],
      "merchantLocationKey": "string",
      "merchantLocationStatus": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fullAddress` | string |  |
| `location.address.city` | string |  |
| `location.address.country` | string |  |
| `location.address.postalCode` | string |  |
| `location.address.stateOrProvince` | string |  |
| `location.locationId` | string |  |
| `locationTypes[]` | string |  |
| `merchantLocationKey` | string |  |
| `merchantLocationStatus` | string |  |
| `name` | string |  |

## Native endpoint

Through the native eBay API, this operation is `GET sell/inventory/v1/location` (base URL `https://api.ebay.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-inventory-locations.md) for the provider-specific parameters and requirements.

