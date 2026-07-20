# QStash: List Schedules

Retrieves all existing schedules from QStash.

```
GET https://connect.mindcloud.co/v1/universal/qStash/latest/actions/list-schedules
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QStash `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qStash/latest/actions/list-schedules?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qStash/latest/actions/list-schedules?${params}`, {
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
      "body": "string",
      "callerIP": "string",
      "createdAt": 1,
      "cron": "string",
      "destination": "string",
      "header": {},
      "isPaused": true,
      "method": "string",
      "parallelism": 1,
      "retries": 1,
      "scheduleId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body` | string |  |
| `callerIP` | string |  |
| `createdAt` | number |  |
| `cron` | string |  |
| `destination` | string |  |
| `header` | object |  |
| `isPaused` | boolean |  |
| `method` | string |  |
| `parallelism` | number |  |
| `retries` | number |  |
| `scheduleId` | string |  |

## Native endpoint

Through the native QStash API, this operation is `GET /v2/schedules` (base URL `https://qstash-eu-central-1.upstash.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-schedules.md) for the provider-specific parameters and requirements.

