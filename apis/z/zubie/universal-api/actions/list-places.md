# Zubie: List Places

Retrieves places from Zubie.

```
GET https://connect.mindcloud.co/v1/universal/zubie/latest/actions/list-places
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zubie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zubie/latest/actions/list-places?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zubie/latest/actions/list-places?${params}`, {
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
      "address": "string",
      "category": "string",
      "key": "string",
      "name": "Ava Chen",
      "radius": 1,
      "updated": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `category` | string |  |
| `key` | string |  |
| `name` | string |  |
| `radius` | number |  |
| `updated` | string |  |

## Native endpoint

Through the native Zubie API, this operation is `GET /places` (base URL `https://api.zubiecar.com/api/v2/zinc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-places.md) for the provider-specific parameters and requirements.

