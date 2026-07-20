# Podio: Get Task

Retrieves an existing task from Podio.

```
GET https://connect.mindcloud.co/v1/universal/podio/latest/actions/get-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Podio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/podio/latest/actions/get-task?connectionId=$CONNECTION_ID&taskId=123456789" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "123456789"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/podio/latest/actions/get-task?${params}`, {
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
| `taskId` | number | yes | The id of the task. Example: `123456789`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comments": [
        {}
      ],
      "completedBy": {},
      "completedOn": "2026-05-07T12:00:00.000Z",
      "completedVia": {},
      "createdBy": {},
      "createdOn": "2026-05-07T12:00:00.000Z",
      "createdVia": {},
      "description": "string",
      "dueDate": "2026-05-07T12:00:00.000Z",
      "dueOn": "2026-05-07T12:00:00.000Z",
      "dueTime": "string",
      "externalId": "string",
      "files": [
        {}
      ],
      "isLiked": true,
      "labels": [
        {}
      ],
      "likeCount": 1,
      "link": "https://example.com",
      "presence": {},
      "private": true,
      "push": {},
      "recurrence": {},
      "ref": {},
      "reminder": {},
      "responsible": {},
      "rights": [
        "string"
      ],
      "spaceId": 1,
      "started": true,
      "status": "string",
      "subscribed": true,
      "subscribedCount": 1,
      "taskId": 1,
      "text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comments` | array<object> |  |
| `completedBy` | object |  |
| `completedOn` | date |  |
| `completedVia` | object |  |
| `createdBy` | object |  |
| `createdOn` | date |  |
| `createdVia` | object |  |
| `description` | string |  |
| `dueDate` | date |  |
| `dueOn` | date |  |
| `dueTime` | string |  |
| `externalId` | string |  |
| `files` | array<object> |  |
| `isLiked` | boolean |  |
| `labels` | array<object> |  |
| `likeCount` | number |  |
| `link` | string |  |
| `presence` | object |  |
| `private` | boolean |  |
| `push` | object |  |
| `recurrence` | object |  |
| `ref` | object |  |
| `reminder` | object |  |
| `responsible` | object |  |
| `rights` | array<string> |  |
| `spaceId` | number |  |
| `started` | boolean |  |
| `status` | string |  |
| `subscribed` | boolean |  |
| `subscribedCount` | number |  |
| `taskId` | number |  |
| `text` | string |  |

## Native endpoint

Through the native Podio API, this operation is `GET /task/:task_id` (base URL `https://api.podio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task.md) for the provider-specific parameters and requirements.

