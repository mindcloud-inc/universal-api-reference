# Qlik: Get Favorites Collection

Retrieves the favorites collection from Qlik.

```
GET https://connect.mindcloud.co/v1/universal/qlik/latest/actions/get-favorites-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Qlik `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qlik/latest/actions/get-favorites-collection?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qlik/latest/actions/get-favorites-collection?${params}`, {
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
      "id": "string",
      "itemCount": 1,
      "name": "Ava Chen",
      "tenantId": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `itemCount` | number |  |
| `name` | string |  |
| `tenantId` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Qlik API, this operation is `GET /api/v1/collections/favorites` (base URL `https://{{credentials.tenantHost}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-favorites-collection.md) for the provider-specific parameters and requirements.

