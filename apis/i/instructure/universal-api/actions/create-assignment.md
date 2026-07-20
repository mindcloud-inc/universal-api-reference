# Instructure: Create Assignment

Creates a new assignment in Instructure Canvas.

```
POST https://connect.mindcloud.co/v1/universal/instructure/latest/actions/create-assignment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instructure `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/instructure/latest/actions/create-assignment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "courseId": "1",
  "name": "MindCloud Validation Assignment"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instructure/latest/actions/create-assignment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "courseId": "1",
    "name": "MindCloud Validation Assignment"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `courseId` | string | yes | The Canvas course ID. Default: `1`. |
| `name` | string | yes | Assignment name. Default: `MindCloud Validation Assignment`. |
| `description` | string | no | Assignment description. Default: `Validator default test payload for Canvas assignment creation metadata.`. |
| `dueAt` | string | no | Assignment due timestamp. |
| `pointsPossible` | number | no | Maximum points possible. Default: `10`. |

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

Through the native Instructure API, this operation is `POST /courses/:course_id/assignments` (base URL `https://canvas.instructure.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-assignment.md) for the provider-specific parameters and requirements.

