# Fabric: List Resource Roots

Retrieves resource roots from Fabric.

```
GET https://connect.mindcloud.co/v1/universal/fabric/latest/actions/list-resource-roots
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fabric `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fabric/latest/actions/list-resource-roots?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fabric/latest/actions/list-resource-roots?${params}`, {
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
      "data": {
        "integrations": [
          {}
        ],
        "resources": {},
        "roots": [
          {}
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `data` | object |  |
| `data.integrations` | array<object> |  |
| `data.resources` | object |  |
| `data.roots` | array<object> |  |

## Native endpoint

Through the native Fabric API, this operation is `GET /v2/resource-roots` (base URL `https://api.fabric.so`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-resource-roots.md) for the provider-specific parameters and requirements.

