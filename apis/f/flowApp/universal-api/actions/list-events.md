# Flow App: List Events



```
GET https://connect.mindcloud.co/v1/universal/flowApp/latest/actions/list-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flow App `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flowApp/latest/actions/list-events?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flowApp/latest/actions/list-events?${params}`, {
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
| `period` | string | no | Return events from one time bucket: current, past, or future. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessStatus": 1,
      "analytics": {},
      "createDate": "string",
      "creator": {},
      "date": "string",
      "description": "string",
      "duration": 1,
      "earlyAccessPeriod": 1,
      "eventToken": "string",
      "onDemandReplays": 1,
      "operators": [
        {}
      ],
      "published": 1,
      "time": "string",
      "timezone": "string",
      "title": "string",
      "token": "string",
      "videoRecord": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessStatus` | number |  |
| `analytics` | object |  |
| `createDate` | string |  |
| `creator` | object |  |
| `date` | string |  |
| `description` | string |  |
| `duration` | number |  |
| `earlyAccessPeriod` | number |  |
| `eventToken` | string |  |
| `onDemandReplays` | number |  |
| `operators` | array<object> |  |
| `published` | number |  |
| `time` | string |  |
| `timezone` | string |  |
| `title` | string |  |
| `token` | string |  |
| `videoRecord` | number |  |

## Native endpoint

Through the native Flow App API, this operation is `GET /events/sessions` (base URL `https://prod.flowapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-events.md) for the provider-specific parameters and requirements.

