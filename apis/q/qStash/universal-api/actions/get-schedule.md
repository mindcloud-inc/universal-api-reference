# QStash: Get Schedule

Retrieves a schedule from QStash by ID.

```
GET https://connect.mindcloud.co/v1/universal/qStash/latest/actions/get-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QStash `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qStash/latest/actions/get-schedule?connectionId=$CONNECTION_ID&scheduleId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "scheduleId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qStash/latest/actions/get-schedule?${params}`, {
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
| `scheduleId` | string | yes | Identifier of the schedule to retrieve. |

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

Through the native QStash API, this operation is `GET /v2/schedules/:scheduleId` (base URL `https://qstash-eu-central-1.upstash.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-schedule.md) for the provider-specific parameters and requirements.

