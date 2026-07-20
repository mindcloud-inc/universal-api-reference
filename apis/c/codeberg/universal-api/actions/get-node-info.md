# Codeberg: Get Node Info



```
GET https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/get-node-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Codeberg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/get-node-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/get-node-info?${params}`, {
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
      "openRegistrations": true,
      "protocols": [
        "string"
      ],
      "services": {
        "inbound": [
          "string"
        ],
        "outbound": [
          "string"
        ]
      },
      "software": {
        "homepage": "https://example.com",
        "name": "Ava Chen",
        "repository": "https://example.com",
        "version": "string"
      },
      "usage": {
        "localComments": 1,
        "localPosts": 1
      },
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `openRegistrations` | boolean |  |
| `protocols` | array<string> |  |
| `services.inbound` | array<string> |  |
| `services.outbound` | array<string> |  |
| `software.homepage` | string |  |
| `software.name` | string |  |
| `software.repository` | string |  |
| `software.version` | string |  |
| `usage.localComments` | number |  |
| `usage.localPosts` | number |  |
| `version` | string |  |

## Native endpoint

Through the native Codeberg API, this operation is `GET /nodeinfo` (base URL `https://codeberg.org/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-node-info.md) for the provider-specific parameters and requirements.

