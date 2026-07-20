# Instructure: Update Assignment

Updates an existing assignment in Instructure Canvas.

```
PUT https://connect.mindcloud.co/v1/universal/instructure/latest/actions/update-assignment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instructure `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/instructure/latest/actions/update-assignment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "courseId": "1",
  "assignmentId": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instructure/latest/actions/update-assignment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "courseId": "1",
    "assignmentId": "1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `courseId` | string | yes | The Canvas course ID. Default: `1`. |
| `assignmentId` | string | yes | The Canvas assignment ID. Default: `1`. |
| `name` | string | no | Assignment name. |
| `description` | string | no | Assignment description. |
| `dueAt` | string | no | Assignment due timestamp. |
| `pointsPossible` | number | no | Maximum points possible. |

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

Through the native Instructure API, this operation is `PUT /courses/:course_id/assignments/:assignment_id` (base URL `https://canvas.instructure.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-assignment.md) for the provider-specific parameters and requirements.

