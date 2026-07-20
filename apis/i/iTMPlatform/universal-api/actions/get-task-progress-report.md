# ITM Platform: Get Task Progress Report



```
GET https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/get-task-progress-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ITM Platform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/get-task-progress-report?connectionId=$CONNECTION_ID&projectId=string&taskId=string&taskProgressId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "taskId": "string",
  "taskProgressId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/get-task-progress-report?${params}`, {
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
| `taskProgressId` | string | yes | The ITM Platform task progress report ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assessmentName": "Ava Chen",
      "assessmentPath": "string",
      "createdBy": "string",
      "projectId": 1,
      "reportDate": "string",
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
| `assessmentName` | string |  |
| `assessmentPath` | string |  |
| `createdBy` | string |  |
| `projectId` | number |  |
| `reportDate` | string |  |
| `taskId` | number |  |
| `taskName` | string |  |
| `taskProgressId` | number |  |

## Native endpoint

Through the native ITM Platform API, this operation is `GET /project/{ProjectId}/task/{TaskId}/progress/{TaskProgressId}` (base URL `https://api.itmplatform.com/{{credentials.company}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task-progress-report.md) for the provider-specific parameters and requirements.

