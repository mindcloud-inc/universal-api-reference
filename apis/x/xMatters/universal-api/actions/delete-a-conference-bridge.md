# xMatters: Delete a conference bridge

Deletes a conference bridge from your xMatters instance.

```
DELETE https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/delete-a-conference-bridge
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/delete-a-conference-bridge?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/delete-a-conference-bridge?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `conferenceBridgeId` | string | no |  |

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

Through the native xMatters API, this operation is `DELETE conference-bridges/{conferenceBridgeId}` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-a-conference-bridge.md) for the provider-specific parameters and requirements.

