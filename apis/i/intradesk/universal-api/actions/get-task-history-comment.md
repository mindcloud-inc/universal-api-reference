# Intradesk: Get Task History Comment

Retrieves a task history comment from Intradesk.

```
GET https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/get-task-history-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intradesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/get-task-history-comment?connectionId=$CONNECTION_ID&taskId=string&historyUid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "string",
  "historyUid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/get-task-history-comment?${params}`, {
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
| `historyUid` | string | yes | History entry UID from Intradesk TaskHistory API path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string |  |

## Native endpoint

Through the native Intradesk API, this operation is `GET /taskhistory/api/v3/Lifetime/{taskId}/{historyUid}/comment` (base URL `https://apigw.intradesk.ru`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task-history-comment.md) for the provider-specific parameters and requirements.

