# Beds24: List Property Rooms

Retrieves property rooms from Beds24.

```
GET https://connect.mindcloud.co/v1/universal/beds24/latest/actions/list-property-rooms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Beds24 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/beds24/latest/actions/list-property-rooms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/beds24/latest/actions/list-property-rooms?${params}`, {
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
      "id": 1,
      "maxPeople": 1,
      "name": "Ava Chen",
      "propertyId": 1,
      "qty": 1,
      "roomType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `maxPeople` | number |  |
| `name` | string |  |
| `propertyId` | number |  |
| `qty` | number |  |
| `roomType` | string |  |

## Native endpoint

Through the native Beds24 API, this operation is `GET /properties/rooms` (base URL `https://beds24.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-property-rooms.md) for the provider-specific parameters and requirements.

