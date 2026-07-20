# Launch27: List Booking Services

Retrieves booking services from Launch27.

```
GET https://connect.mindcloud.co/v1/universal/launch27/latest/actions/list-booking-services
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Launch27 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/launch27/latest/actions/list-booking-services?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/launch27/latest/actions/list-booking-services?${params}`, {
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
      "commercial": true,
      "discount_by_code": true,
      "discount_by_frequency": true,
      "id": 1,
      "name": "Ava Chen",
      "price": 1,
      "tags_info": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `commercial` | boolean |  |
| `discount_by_code` | boolean |  |
| `discount_by_frequency` | boolean |  |
| `id` | number |  |
| `name` | string |  |
| `price` | number |  |
| `tags_info` | object |  |

## Native endpoint

Through the native Launch27 API, this operation is `GET booking/services` (base URL `https://{{credentials.subdomain}}.launch27.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-booking-services.md) for the provider-specific parameters and requirements.

