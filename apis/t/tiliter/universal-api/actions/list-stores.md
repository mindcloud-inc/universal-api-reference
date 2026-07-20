# Tiliter: List Stores

Retrieves stores from the Tiliter Recognition API.

```
GET https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/list-stores
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tiliter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/list-stores?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/list-stores?${params}`, {
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
      "stores": [
        {
          "areaCode": "string",
          "country": "string",
          "friendlyName": "Ava Chen",
          "region": "string",
          "storeId": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `stores` | array<object> |  |
| `stores[].areaCode` | string |  |
| `stores[].country` | string |  |
| `stores[].friendlyName` | string |  |
| `stores[].region` | string |  |
| `stores[].storeId` | string |  |

## Native endpoint

Through the native Tiliter API, this operation is `GET /stores/` (base URL `https://recognition.services.tiliter.com/v1/15`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-stores.md) for the provider-specific parameters and requirements.

