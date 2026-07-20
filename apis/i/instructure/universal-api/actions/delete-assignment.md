# Instructure: Delete Assignment

Deletes an assignment from Instructure Canvas.

```
DELETE https://connect.mindcloud.co/v1/universal/instructure/latest/actions/delete-assignment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instructure `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/instructure/latest/actions/delete-assignment?connectionId=$CONNECTION_ID&assignmentId=1&courseId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "assignmentId": "1",
  "courseId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instructure/latest/actions/delete-assignment?${params}`, {
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
| `assignmentId` | string | yes | The Canvas assignment ID. Default: `1`. |
| `courseId` | string | yes | The Canvas course ID. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "courseId": 1,
      "description": "string",
      "dueAt": "string",
      "htmlUrl": "https://example.com",
      "id": 1,
      "lockAt": "string",
      "name": "Ava Chen",
      "pointsPossible": 1,
      "published": true,
      "unlockAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `courseId` | number |  |
| `description` | string |  |
| `dueAt` | string |  |
| `htmlUrl` | string |  |
| `id` | number |  |
| `lockAt` | string |  |
| `name` | string |  |
| `pointsPossible` | number |  |
| `published` | boolean |  |
| `unlockAt` | string |  |

## Native endpoint

Through the native Instructure API, this operation is `DELETE /courses/:course_id/assignments/:assignment_id` (base URL `https://canvas.instructure.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-assignment.md) for the provider-specific parameters and requirements.

