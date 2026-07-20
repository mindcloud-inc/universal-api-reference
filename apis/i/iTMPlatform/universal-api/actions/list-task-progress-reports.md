# ITM Platform: List Task Progress Reports



```
GET https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/list-task-progress-reports
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ITM Platform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/list-task-progress-reports?connectionId=$CONNECTION_ID&projectId=string&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/list-task-progress-reports?${params}`, {
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
| `projectId` | string | yes | The ITM Platform project ID. |
| `taskId` | string | yes | The ITM Platform task ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assessment": {},
      "detailDescription": "string",
      "percentageCompleted": 1,
      "projectId": 1,
      "shortDescription": "string",
      "taskId": 1,
      "taskName": "Ava Chen",
      "taskProgressId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assessment` | object |  |
| `detailDescription` | string |  |
| `percentageCompleted` | number |  |
| `projectId` | number |  |
| `shortDescription` | string |  |
| `taskId` | number |  |
| `taskName` | string |  |
| `taskProgressId` | number |  |

## Native endpoint

Through the native ITM Platform API, this operation is `GET /project/{ProjectId}/task/{TaskId}/progress/` (base URL `https://api.itmplatform.com/{{credentials.company}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-task-progress-reports.md) for the provider-specific parameters and requirements.

