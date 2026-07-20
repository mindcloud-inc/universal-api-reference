# Teach 'n Go: Add Student Note

Creates a student note in Teach 'n Go.

```
POST https://connect.mindcloud.co/v1/universal/teachNGo/latest/actions/add-student-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teach 'n Go `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/teachNGo/latest/actions/add-student-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "studentId": "string",
  "visibility": "string",
  "note": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/teachNGo/latest/actions/add-student-note', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "studentId": "string",
    "visibility": "string",
    "note": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `studentId` | string | yes | The student record that should receive the note. |
| `visibility` | string | yes | Set to public or private. |
| `note` | string | yes | The note content to add to the student record. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Teach 'n Go API returns.

## Native endpoint

Through the native Teach 'n Go API, this operation is `POST /api/v1/note/add` (base URL `https://app.teachngo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-student-note.md) for the provider-specific parameters and requirements.

