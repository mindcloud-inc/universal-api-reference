# Socket: Calculate Settings

Retrieves current settings for requested Socket organizations.

```
POST https://connect.mindcloud.co/v1/universal/socket/latest/actions/calculate-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socket `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/socket/latest/actions/calculate-settings" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/socket/latest/actions/calculate-settings', {
  method: 'POST',
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
      "defaults": {
        "issueRules": {}
      },
      "entries": [
        {
          "settings": {},
          "start": "string"
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
| `defaults` | object |  |
| `defaults.issueRules` | object |  |
| `entries` | array<object> |  |
| `entries[]` | object |  |
| `entries[].settings` | object |  |
| `entries[].start` | string |  |

## Native endpoint

Through the native Socket API, this operation is `POST /settings` (base URL `https://api.socket.dev/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/calculate-settings.md) for the provider-specific parameters and requirements.

