# Intradesk: List Task History

Retrieves task history entries from Intradesk.

```
GET https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/list-task-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intradesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/list-task-history?connectionId=$CONNECTION_ID&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/list-task-history?${params}`, {
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
| `taskId` | string | yes | Task identifier from Intradesk TaskHistory API path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "isVisitedOtherGlobal": true,
      "isVisitedSelfGlobal": true,
      "nextInfo": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `isVisitedOtherGlobal` | boolean |  |
| `isVisitedSelfGlobal` | boolean |  |
| `nextInfo` | object |  |

## Native endpoint

Through the native Intradesk API, this operation is `GET /taskhistory/api/v3/Lifetime/{taskid}/full` (base URL `https://apigw.intradesk.ru`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-task-history.md) for the provider-specific parameters and requirements.

