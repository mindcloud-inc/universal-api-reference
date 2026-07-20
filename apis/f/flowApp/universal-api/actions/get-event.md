# Flow App: Get Event



```
GET https://connect.mindcloud.co/v1/universal/flowApp/latest/actions/get-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flow App `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flowApp/latest/actions/get-event?connectionId=$CONNECTION_ID&sessionToken=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sessionToken": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flowApp/latest/actions/get-event?${params}`, {
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
| `sessionToken` | string | yes | The unique identifier for the event session you want to look up. |

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
      "feedbackQuestions": [
        {}
      ],
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
| `feedbackQuestions` | array<object> |  |
| `onDemandReplays` | number |  |
| `operators` | array<object> |  |
| `published` | number |  |
| `time` | string |  |
| `timezone` | string |  |
| `title` | string |  |
| `token` | string |  |
| `videoRecord` | number |  |

## Native endpoint

Through the native Flow App API, this operation is `GET /events/sessions/:sessionToken` (base URL `https://prod.flowapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event.md) for the provider-specific parameters and requirements.

