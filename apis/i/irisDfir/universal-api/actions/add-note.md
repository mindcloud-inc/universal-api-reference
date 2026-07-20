# Iris Dfir: Add Note



```
POST https://connect.mindcloud.co/v1/universal/irisDfir/latest/actions/add-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Iris Dfir `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/irisDfir/latest/actions/add-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "directoryId": 1,
  "noteTitle": "string",
  "noteContent": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/irisDfir/latest/actions/add-note', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "directoryId": 1,
    "noteTitle": "string",
    "noteContent": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `directoryId` | number | yes | IRIS note directory identifier. |
| `noteTitle` | string | yes | Title of the note. |
| `noteContent` | string | yes | Content of the note. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "comments": [
          {}
        ],
        "custom_attributes": {},
        "directory_id": 1,
        "directory": {
          "case_id": 1,
          "id": 1,
          "name": "Ava Chen",
          "parent_id": 1
        },
        "modification_history": {},
        "note_case_id": 1,
        "note_content": "string",
        "note_creationdate": "2026-05-07T12:00:00.000Z",
        "note_id": 1,
        "note_lastupdate": "2026-05-07T12:00:00.000Z",
        "note_title": "string",
        "note_user": 1,
        "note_uuid": "string"
      },
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.comments` | array<object> |  |
| `data.custom_attributes` | object |  |
| `data.directory_id` | number |  |
| `data.directory.case_id` | number |  |
| `data.directory.id` | number |  |
| `data.directory.name` | string |  |
| `data.directory.parent_id` | number |  |
| `data.modification_history` | object |  |
| `data.note_case_id` | number |  |
| `data.note_content` | string |  |
| `data.note_creationdate` | date |  |
| `data.note_id` | number |  |
| `data.note_lastupdate` | date |  |
| `data.note_title` | string |  |
| `data.note_user` | number |  |
| `data.note_uuid` | string |  |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Iris Dfir API, this operation is `POST /case/notes/add` (base URL `https://v200.beta.dfir-iris.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-note.md) for the provider-specific parameters and requirements.

