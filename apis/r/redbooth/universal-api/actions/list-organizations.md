# Redbooth: List Organizations

Retrieves organizations from Redbooth.

```
GET https://connect.mindcloud.co/v1/universal/redbooth/latest/actions/list-organizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Redbooth `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/redbooth/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/redbooth/latest/actions/list-organizations?${params}`, {
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
      "domain": "string",
      "enable_privacy": true,
      "enable_time_tracking": true,
      "id": 1,
      "name": "Ava Chen",
      "permalink": "https://example.com",
      "product": "string",
      "product_name": "Ava Chen",
      "remaining_users": 1,
      "seats": 1,
      "type": "string",
      "used_users": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `domain` | string |  |
| `enable_privacy` | boolean |  |
| `enable_time_tracking` | boolean |  |
| `id` | number |  |
| `name` | string |  |
| `permalink` | string |  |
| `product` | string |  |
| `product_name` | string |  |
| `remaining_users` | number |  |
| `seats` | number |  |
| `type` | string |  |
| `used_users` | number |  |

## Native endpoint

Through the native Redbooth API, this operation is `GET /organizations` (base URL `https://redbooth.com/api/3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-organizations.md) for the provider-specific parameters and requirements.

