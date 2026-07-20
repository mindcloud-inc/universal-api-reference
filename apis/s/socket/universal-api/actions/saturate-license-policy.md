# Socket: Saturate License Policy

Retrieves a saturated Socket license policy.

```
PUT https://connect.mindcloud.co/v1/universal/socket/latest/actions/saturate-license-policy
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socket `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/socket/latest/actions/saturate-license-policy" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/socket/latest/actions/saturate-license-policy', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "allow": {
        "classes": [
          "string"
        ],
        "disjs": [
          "string"
        ],
        "packageURLs": [
          "https://example.com"
        ],
        "strings": [
          "string"
        ]
      },
      "monitor": {
        "classes": [
          "string"
        ],
        "disjs": [
          "string"
        ],
        "packageURLs": [
          "https://example.com"
        ],
        "strings": [
          "string"
        ]
      },
      "warn": {
        "classes": [
          "string"
        ],
        "disjs": [
          "string"
        ],
        "packageURLs": [
          "https://example.com"
        ],
        "strings": [
          "string"
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
| `allow` | object |  |
| `allow.classes` | array<string> |  |
| `allow.disjs` | array<string> |  |
| `allow.packageURLs` | array<string> |  |
| `allow.strings` | array<string> |  |
| `monitor` | object |  |
| `monitor.classes` | array<string> |  |
| `monitor.disjs` | array<string> |  |
| `monitor.packageURLs` | array<string> |  |
| `monitor.strings` | array<string> |  |
| `warn` | object |  |
| `warn.classes` | array<string> |  |
| `warn.disjs` | array<string> |  |
| `warn.packageURLs` | array<string> |  |
| `warn.strings` | array<string> |  |

## Native endpoint

Through the native Socket API, this operation is `POST /saturate-license-policy` (base URL `https://api.socket.dev/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/saturate-license-policy.md) for the provider-specific parameters and requirements.

