# inFlow Inventory: List Locations

Retrieves location records from inFlow Inventory.

```
GET https://connect.mindcloud.co/v1/universal/inFlowInventory/latest/actions/list-locations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a inFlow Inventory `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/inFlowInventory/latest/actions/list-locations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/inFlowInventory/latest/actions/list-locations?${params}`, {
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
        "address1": "string",
        "address2": "string",
        "addressType": "string",
        "city": "string",
        "country": "string",
        "postalCode": "string",
        "remarks": "string",
        "state": "string"
      },
      "isActive": true,
      "isDefault": true,
      "locationId": "string",
      "name": "Ava Chen",
      "timestamp": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address.address1` | string |  |
| `address.address2` | string |  |
| `address.addressType` | string |  |
| `address.city` | string |  |
| `address.country` | string |  |
| `address.postalCode` | string |  |
| `address.remarks` | string |  |
| `address.state` | string |  |
| `isActive` | boolean |  |
| `isDefault` | boolean |  |
| `locationId` | string |  |
| `name` | string |  |
| `timestamp` | string |  |

## Native endpoint

Through the native inFlow Inventory API, this operation is `GET /locations` (base URL `https://cloudapi.inflowinventory.com/{{credentials.companyId}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-locations.md) for the provider-specific parameters and requirements.

