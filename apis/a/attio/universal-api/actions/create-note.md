# Attio: Create Note

Creates a note in Attio.

```
POST https://connect.mindcloud.co/v1/universal/attio/latest/actions/create-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Attio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/attio/latest/actions/create-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "parentObject": "people",
  "parentRecordId": "891dcbfc-9141-415d-9b2a-2238a6cc012d",
  "title": "Initial Prospecting Call Summary",
  "content": "# Meeting Recap\\n\\n- Reviewed Q3 metrics\\n- Agreed next steps"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/attio/latest/actions/create-note', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "parentObject": "people",
    "parentRecordId": "891dcbfc-9141-415d-9b2a-2238a6cc012d",
    "title": "Initial Prospecting Call Summary",
    "content": "# Meeting Recap\\n\\n- Reviewed Q3 metrics\\n- Agreed next steps"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `parentObject` | string | yes | The ID or slug of the parent object the note belongs to. Example: `people`. |
| `parentRecordId` | string | yes | The ID of the parent record the note belongs to. Example: `891dcbfc-9141-415d-9b2a-2238a6cc012d`. |
| `title` | string | yes | The note title. The title is plaintext only and has no formatting. Example: `Initial Prospecting Call Summary`. |
| `format` | list<string> | no | Specify the format for the note content. Defaults to plaintext; choose markdown for rich formatting. One of: `markdown`, `plaintext`. Default: `plaintext`. |
| `content` | string | yes | The main content of the note, formatted according to the format field. Example: `# Meeting Recap\n\n- Reviewed Q3 metrics\n- Agreed next steps`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `createdAt` | date | no | Optional backdated created-at timestamp in ISO 8601 format. Example: `2023-01-01T15:00:00.000Z`. |
| `meetingId` | string | no | Optional meeting to associate with the note. Example: `14beef7a-99f7-4534-a87e-70b564330a4c`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentMarkdown": "string",
      "contentPlaintext": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdByActor": {},
      "id": {},
      "parentObject": "string",
      "parentRecordId": "string",
      "tags": [
        "string"
      ],
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentMarkdown` | string | Markdown note content. |
| `contentPlaintext` | string | Plaintext note content. |
| `createdAt` | date | When the note was created. |
| `createdByActor` | object | Actor that created the note. |
| `id` | object | Note identifier payload containing workspace and note ids. |
| `parentObject` | string | Parent object slug for the note. |
| `parentRecordId` | string | Parent record id linked to the note. |
| `tags` | array<string> | Tags attached to the note. |
| `title` | string | Title of the note. |

## Native endpoint

Through the native Attio API, this operation is `POST /v2/notes` (base URL `https://api.attio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-note.md) for the provider-specific parameters and requirements.

