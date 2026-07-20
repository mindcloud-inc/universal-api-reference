# Beds24: List Room Availability

Retrieves room availability dates from Beds24.

```
GET https://connect.mindcloud.co/v1/universal/beds24/latest/actions/list-room-availability
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Beds24 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/beds24/latest/actions/list-room-availability?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/beds24/latest/actions/list-room-availability?${params}`, {
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
      "availability": {},
      "name": "Ava Chen",
      "propertyId": 1,
      "roomId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availability` | object |  |
| `name` | string |  |
| `propertyId` | number |  |
| `roomId` | number |  |

## Native endpoint

Through the native Beds24 API, this operation is `GET /inventory/rooms/availability` (base URL `https://beds24.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-room-availability.md) for the provider-specific parameters and requirements.

