# Ipregistry: Parse User Agents



```
GET https://connect.mindcloud.co/v1/universal/ipregistry/latest/actions/parse-user-agents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ipregistry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ipregistry/latest/actions/parse-user-agents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ipregistry/latest/actions/parse-user-agents?${params}`, {
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
      "results": [
        {
          "device": {
            "name": "Ava Chen",
            "type": "string"
          },
          "engine": {
            "name": "Ava Chen",
            "type": "string",
            "version": "string",
            "version_major": "string"
          },
          "header": "string",
          "name": "Ava Chen",
          "os": {
            "name": "Ava Chen",
            "type": "string",
            "version": "string"
          },
          "type": "string",
          "version": "string",
          "version_major": "string"
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
| `results` | array<object> |  |
| `results[]` | object |  |
| `results[].device` | object |  |
| `results[].device.name` | string |  |
| `results[].device.type` | string |  |
| `results[].engine` | object |  |
| `results[].engine.name` | string |  |
| `results[].engine.type` | string |  |
| `results[].engine.version` | string |  |
| `results[].engine.version_major` | string |  |
| `results[].header` | string |  |
| `results[].name` | string |  |
| `results[].os` | object |  |
| `results[].os.name` | string |  |
| `results[].os.type` | string |  |
| `results[].os.version` | string |  |
| `results[].type` | string |  |
| `results[].version` | string |  |
| `results[].version_major` | string |  |

## Native endpoint

Through the native Ipregistry API, this operation is `POST /user_agent` (base URL `https://api.ipregistry.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/parse-user-agents.md) for the provider-specific parameters and requirements.

