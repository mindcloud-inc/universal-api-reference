# Browse AI: List Bulk Runs

Retrieves bulk runs from Browse AI.

```
GET https://connect.mindcloud.co/v1/universal/browseAI/latest/actions/list-bulk-runs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Browse AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/browseAI/latest/actions/list-bulk-runs?connectionId=$CONNECTION_ID&robotId=c3689adb-50aa-44af-b265-a7e0d4e5846e" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "robotId": "c3689adb-50aa-44af-b265-a7e0d4e5846e"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/browseAI/latest/actions/list-bulk-runs?${params}`, {
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
| `robotId` | string | yes | Unique robot ID You can find a robot's ID by opening it on the dashboard and copying its ID in the browser address bar. Example: `c3689adb-50aa-44af-b265-a7e0d4e5846e`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `page` | number | no | Page number Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": 1,
      "failedTasks": 1,
      "id": "string",
      "robotId": "string",
      "status": "string",
      "successfulTasks": 1,
      "tasksCount": 1,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | number | Bulk run creation date and time in the form of a Unix timestamp. |
| `failedTasks` | number | Number of failed tasks under this bulk run. |
| `id` | string | Unique bulk run ID |
| `robotId` | string | Unique robot ID |
| `status` | string | The status of the bulk run. |
| `successfulTasks` | number | Number of successfully finished tasks under this bulk run. |
| `tasksCount` | number | Total number of tasks under this bulk run. |
| `title` | string | An optional string that describes the bulk run. |

## Native endpoint

Through the native Browse AI API, this operation is `GET /robots/:robotId/bulk-runs` (base URL `https://api.browse.ai/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-bulk-runs.md) for the provider-specific parameters and requirements.

