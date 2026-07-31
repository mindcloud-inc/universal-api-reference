# D&D 5e: List Equipment



```
GET https://connect.mindcloud.co/v1/universal/dD5e/latest/actions/list-equipment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a D&D 5e `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dD5e/latest/actions/list-equipment?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dD5e/latest/actions/list-equipment?${params}`, {
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
      "results": [
        {
          "index": "string",
          "name": "Ava Chen",
          "url": "https://example.com"
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
| `count` | number |  |
| `results` | array<object> |  |
| `results[].index` | string |  |
| `results[].name` | string |  |
| `results[].url` | string |  |

## Native endpoint

Through the native D&D 5e API, this operation is `GET /equipment` (base URL `https://www.dnd5eapi.co/api/2014`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-equipment.md) for the provider-specific parameters and requirements.

