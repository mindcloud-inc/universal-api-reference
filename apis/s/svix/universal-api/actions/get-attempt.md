# Svix: Get Attempt

Retrieves a specific delivery attempt from Svix.

```
GET https://connect.mindcloud.co/v1/universal/svix/latest/actions/get-attempt
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Svix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/svix/latest/actions/get-attempt?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/svix/latest/actions/get-attempt?${params}`, {
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
      "endpointId": "string",
      "id": "string",
      "msg": {},
      "msgId": "string",
      "response": "string",
      "responseDurationMs": 1,
      "responseStatusCode": 1,
      "status": 1,
      "statusText": "string",
      "timestamp": "string",
      "triggerType": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `endpointId` | string |  |
| `id` | string |  |
| `msg` | object |  |
| `msgId` | string |  |
| `response` | string |  |
| `responseDurationMs` | number |  |
| `responseStatusCode` | number |  |
| `status` | number |  |
| `statusText` | string |  |
| `timestamp` | string |  |
| `triggerType` | number |  |
| `url` | string |  |

## Native endpoint

Through the native Svix API, this operation is `GET /api/v1/app/{app_id}/msg/{msg_id}/attempt/{attempt_id}` (base URL `https://api.us.svix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-attempt.md) for the provider-specific parameters and requirements.

