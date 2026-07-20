# xMatters: Modify a conference bridge

Updates a conference bridge in your xMatters instance.

```
PUT https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/modify-a-conference-bridge
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/modify-a-conference-bridge" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/modify-a-conference-bridge', {
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
      "description": "string",
      "id": "string",
      "links": {
        "self": "https://example.com"
      },
      "meetingLink": "https://example.com",
      "name": "Ava Chen",
      "pauseBeforeBridgePrompt": 1,
      "preferredConnectionType": "string",
      "staticBridgeNumber": true,
      "tollFreeNumber": "string",
      "tollNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `id` | string |  |
| `links.self` | string |  |
| `meetingLink` | string |  |
| `name` | string |  |
| `pauseBeforeBridgePrompt` | number |  |
| `preferredConnectionType` | string |  |
| `staticBridgeNumber` | boolean |  |
| `tollFreeNumber` | string |  |
| `tollNumber` | string |  |

## Native endpoint

Through the native xMatters API, this operation is `POST conference-bridges` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/modify-a-conference-bridge.md) for the provider-specific parameters and requirements.

