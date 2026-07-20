# Ipregistry: Parse Origin User Agent



```
GET https://connect.mindcloud.co/v1/universal/ipregistry/latest/actions/parse-origin-user-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ipregistry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ipregistry/latest/actions/parse-origin-user-agent?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ipregistry/latest/actions/parse-origin-user-agent?${params}`, {
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
      "device": {
        "brand": "string",
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
        "type": "string"
      },
      "type": "string",
      "version": "string",
      "version_major": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `device` | object |  |
| `device.brand` | string |  |
| `device.name` | string |  |
| `device.type` | string |  |
| `engine` | object |  |
| `engine.name` | string |  |
| `engine.type` | string |  |
| `engine.version` | string |  |
| `engine.version_major` | string |  |
| `header` | string |  |
| `name` | string |  |
| `os` | object |  |
| `os.name` | string |  |
| `os.type` | string |  |
| `type` | string |  |
| `version` | string |  |
| `version_major` | string |  |

## Native endpoint

Through the native Ipregistry API, this operation is `GET /user_agent` (base URL `https://api.ipregistry.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/parse-origin-user-agent.md) for the provider-specific parameters and requirements.

