# Reach360: Unenroll User From Course

Removes a user from a Reach360 course.

```
DELETE https://connect.mindcloud.co/v1/universal/reach360/latest/actions/unenroll-user-from-course
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reach360 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/reach360/latest/actions/unenroll-user-from-course?connectionId=$CONNECTION_ID&courseId=string&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "courseId": "string",
  "userId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reach360/latest/actions/unenroll-user-from-course?${params}`, {
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
| `courseId` | string | yes | The course ID. |
| `userId` | string | yes | The user ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Reach360 API returns.

## Native endpoint

Through the native Reach360 API, this operation is `DELETE /courses/:courseId/users/:userId` (base URL `https://api.reach360.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unenroll-user-from-course.md) for the provider-specific parameters and requirements.

