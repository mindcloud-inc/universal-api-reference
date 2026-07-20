# Reach360: Import Course Completion

Imports a user's course completion into Reach360.

```
POST https://connect.mindcloud.co/v1/universal/reach360/latest/actions/import-course-completion
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reach360 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/reach360/latest/actions/import-course-completion" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "courseId": "string",
  "userId": "string",
  "startedAt": "2026-05-07T12:00:00.000Z",
  "completedAt": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/reach360/latest/actions/import-course-completion', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "courseId": "string",
    "userId": "string",
    "startedAt": "2026-05-07T12:00:00.000Z",
    "completedAt": "2026-05-07T12:00:00.000Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `courseId` | string | yes | The course ID. |
| `userId` | string | yes | The user ID. |
| `startedAt` | date | yes | When the user started the course. |
| `completedAt` | date | yes | When the user completed the course. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Reach360 API returns.

## Native endpoint

Through the native Reach360 API, this operation is `POST /courses/:courseId/users/:userId/completions` (base URL `https://api.reach360.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/import-course-completion.md) for the provider-specific parameters and requirements.

