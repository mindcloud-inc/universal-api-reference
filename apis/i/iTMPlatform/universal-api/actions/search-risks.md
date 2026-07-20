# ITM Platform: Search Risks



```
GET https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/search-risks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ITM Platform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/search-risks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/search-risks?${params}`, {
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
      "description": "string",
      "id": 1,
      "impact": {},
      "level": {},
      "name": "Ava Chen",
      "probability": {},
      "status": {},
      "type": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `id` | number |  |
| `impact` | object |  |
| `level` | object |  |
| `name` | string |  |
| `probability` | object |  |
| `status` | object |  |
| `type` | object |  |

## Native endpoint

Through the native ITM Platform API, this operation is `GET /v2/risks/search` (base URL `https://api.itmplatform.com/{{credentials.company}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-risks.md) for the provider-specific parameters and requirements.

