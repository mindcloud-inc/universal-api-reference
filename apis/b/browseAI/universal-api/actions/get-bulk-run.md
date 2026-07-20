# Browse AI: Get Bulk Run

Retrieves a bulk run from Browse AI.

```
GET https://connect.mindcloud.co/v1/universal/browseAI/latest/actions/get-bulk-run
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Browse AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/browseAI/latest/actions/get-bulk-run?connectionId=$CONNECTION_ID&robotId=c3689adb-50aa-44af-b265-a7e0d4e5846e&bulkRunId=5aa4df52-25bb-48da-bf38-ce4f2bd98dd5" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "robotId": "c3689adb-50aa-44af-b265-a7e0d4e5846e",
  "bulkRunId": "5aa4df52-25bb-48da-bf38-ce4f2bd98dd5"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/browseAI/latest/actions/get-bulk-run?${params}`, {
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
| `bulkRunId` | string | yes | Unique bulk run ID Example: `5aa4df52-25bb-48da-bf38-ce4f2bd98dd5`. |

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
      "bulkRun": {},
      "robotTasks": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bulkRun` | object |  |
| `robotTasks` | object | A paginated list of tasks. |

## Native endpoint

Through the native Browse AI API, this operation is `GET /robots/:robotId/bulk-runs/:bulkRunId` (base URL `https://api.browse.ai/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bulk-run.md) for the provider-specific parameters and requirements.

