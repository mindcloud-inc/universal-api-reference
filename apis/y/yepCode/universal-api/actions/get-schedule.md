# YepCode: Get scheduled process

Retrieves a scheduled process from YepCode.

```
GET https://connect.mindcloud.co/v1/universal/yepCode/latest/actions/get-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YepCode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yepCode/latest/actions/get-schedule?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yepCode/latest/actions/get-schedule?${params}`, {
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
| `id` | string | yes | Unique identifier of the scheduled process to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comment": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "cron": "string",
      "dateTime": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "paused": true,
      "processId": "string",
      "settings": {
        "agentPoolSlugs": [
          "string"
        ],
        "allowConcurrentExecutions": true
      },
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "updatedBy": "string",
      "versionId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comment` | string | Comment for the scheduled process |
| `createdAt` | date | Timestamp when the scheduled process was created |
| `createdBy` | string | Username of the user who created the scheduled process |
| `cron` | string | Cron expression for periodic schedules |
| `dateTime` | date | Execution date and time for one-time schedules |
| `id` | string | Unique identifier (UUID) of the scheduled process |
| `paused` | boolean | Whether the schedule is currently paused |
| `processId` | string | Unique identifier (UUID) of the process that is scheduled |
| `settings.agentPoolSlugs` | array<string> | Agent pools used for scheduled executions |
| `settings.allowConcurrentExecutions` | boolean | Whether concurrent executions are allowed |
| `type` | string | Type of scheduled process |
| `updatedAt` | date | Timestamp when the scheduled process was last updated |
| `updatedBy` | string | Username of the user who last updated the scheduled process |
| `versionId` | string | Version tag or alias of the process version to execute |

## Native endpoint

Through the native YepCode API, this operation is `GET /schedules/:id` (base URL `https://cloud.yepcode.io/api/{{credentials.team}}/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-schedule.md) for the provider-specific parameters and requirements.

