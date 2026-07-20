# Control D: List Service Categories

Retrieves service categories from Control D.

```
GET https://connect.mindcloud.co/v1/universal/controlD/latest/actions/list-service-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Control D `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/controlD/latest/actions/list-service-categories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/controlD/latest/actions/list-service-categories?${params}`, {
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
      "count": 1,
      "description": "string",
      "name": "Ava Chen",
      "PK": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `description` | string |  |
| `name` | string |  |
| `PK` | string |  |

## Native endpoint

Through the native Control D API, this operation is `GET /services/categories` (base URL `https://api.controld.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-service-categories.md) for the provider-specific parameters and requirements.

