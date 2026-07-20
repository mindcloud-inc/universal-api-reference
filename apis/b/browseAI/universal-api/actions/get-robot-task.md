# Browse AI: Get Robot Task

Retrieves a robot task from Browse AI.

```
GET https://connect.mindcloud.co/v1/universal/browseAI/latest/actions/get-robot-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Browse AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/browseAI/latest/actions/get-robot-task?connectionId=$CONNECTION_ID&robotId=c3689adb-50aa-44af-b265-a7e0d4e5846e&taskId=f3672790-4561-424b-8a7b-7b7df182b236" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "robotId": "c3689adb-50aa-44af-b265-a7e0d4e5846e",
  "taskId": "f3672790-4561-424b-8a7b-7b7df182b236"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/browseAI/latest/actions/get-robot-task?${params}`, {
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
| `taskId` | string | yes | Unique task ID Example: `f3672790-4561-424b-8a7b-7b7df182b236`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "capturedDataTemporaryUrl": "https://example.com",
      "capturedLists": {},
      "capturedScreenshots": {},
      "capturedTexts": {},
      "createdAt": 1,
      "finishedAt": 1,
      "id": "string",
      "inputParameters": {},
      "retriedByTaskId": "string",
      "retriedOriginalTaskId": "string",
      "robotBulkRunId": "string",
      "robotId": "string",
      "runByAPI": true,
      "runByTaskMonitorId": "string",
      "runByUserId": "string",
      "startedAt": 1,
      "status": "string",
      "triedRecordingVideo": true,
      "userFriendlyError": "string",
      "videoRemovedAt": 1,
      "videoUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `capturedDataTemporaryUrl` | string | If your task's captured data exceeds 100KB, the data will be only accessible through this link. There's a 24 hours expiration time for this link (you need to call this API again to get a new link if it expires). |
| `capturedLists` | object | All lists captured in this task. |
| `capturedScreenshots` | object | All screenshots captured in this task. |
| `capturedTexts` | object | Captured texts |
| `createdAt` | number | Task creation date and time in the form of a Unix timestamp |
| `finishedAt` | number | Task finish date and time in the form of a Unix timestamp.  If `null`, it means robot is still running and capturing data.  Tasks time out with an error if they are not finished within 15 minutes (or the maximum duration allowed on your plan). |
| `id` | string | Unique task ID |
| `inputParameters` | object | An object of input parameters to override default input parameters. |
| `retriedByTaskId` | string | The ID of the task that retried this task, if this task failed with an error and was retried.  Failed tasks get retried if "Double Check" option is enabled on robot Settings page. "Double Check" is enabled by default. |
| `retriedOriginalTaskId` | string | The ID of the original failed task this task was retrying. For example, if task A failed and was retried by task B, and task B was retried by task C, `retriedOriginalTaskId` will point to task A in both task B and C. |
| `robotBulkRunId` | string | Robot bulk run ID associated with this task |
| `robotId` | string | Unique robot ID |
| `runByAPI` | boolean | Whether the robot was ran through the API |
| `runByTaskMonitorId` | string | Monitor ID that ran this check |
| `runByUserId` | string | User ID who ran the robot on the dashboard |
| `startedAt` | number | Task start date and time in the form of a Unix timestamp |
| `status` | string | task status |
| `triedRecordingVideo` | boolean | Whether the robot tried to record a video while performing this task.  You can change a robot's video recording setting on its Settings page.   Robots try to record a video when a task is failed and auto-retried as well. |
| `userFriendlyError` | string | If task fails, a user-friendly error will be provided here. |
| `videoRemovedAt` | number | After your account's data retention period, task videos get removed and  this field will be video removal date and time in the form of a Unix timestamp. |
| `videoUrl` | string | If a video was recorded for this task, this is the link to the video. |

## Native endpoint

Through the native Browse AI API, this operation is `GET /robots/:robotId/tasks/:taskId` (base URL `https://api.browse.ai/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-robot-task.md) for the provider-specific parameters and requirements.

