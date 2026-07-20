# Browse AI: Check System Status

Retrieves system status from Browse AI.

```
GET https://connect.mindcloud.co/v1/universal/browseAI/latest/actions/check-system-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Browse AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/browseAI/latest/actions/check-system-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/browseAI/latest/actions/check-system-status?${params}`, {
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
      "messageCode": "string",
      "statusCode": 1,
      "tasksQueueStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `messageCode` | string |  |
| `statusCode` | number |  |
| `tasksQueueStatus` | string |  |

## Native endpoint

Through the native Browse AI API, this operation is `GET /status` (base URL `https://api.browse.ai/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-system-status.md) for the provider-specific parameters and requirements.

