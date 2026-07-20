# Orderry: List Services

Retrieves a list of services from Orderry.

```
GET https://connect.mindcloud.co/v1/universal/orderry/latest/actions/list-services
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Orderry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orderry/latest/actions/list-services?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orderry/latest/actions/list-services?${params}`, {
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
      "name": "Ava Chen",
      "price": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `name` | string |  |
| `price` | number |  |

## Native endpoint

Through the native Orderry API, this operation is `GET services/` (base URL `https://api.orderry.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-services.md) for the provider-specific parameters and requirements.

