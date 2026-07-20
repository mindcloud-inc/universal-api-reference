# xMatters: Get a conference bridge

Retrieves a conference bridge from your xMatters instance.

```
GET https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-a-conference-bridge
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-a-conference-bridge?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-a-conference-bridge?${params}`, {
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
      "count": 1,
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
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `data[].description` | string |  |
| `data[].id` | string |  |
| `data[].links.self` | string |  |
| `data[].meetingLink` | string |  |
| `data[].name` | string |  |
| `data[].pauseBeforeBridgePrompt` | number |  |
| `data[].preferredConnectionType` | string |  |
| `data[].staticBridgeNumber` | boolean |  |
| `data[].tollFreeNumber` | string |  |
| `data[].tollNumber` | string |  |
| `total` | number |  |

## Native endpoint

Through the native xMatters API, this operation is `GET conference-bridges/{conferenceBridgeId}` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-a-conference-bridge.md) for the provider-specific parameters and requirements.

