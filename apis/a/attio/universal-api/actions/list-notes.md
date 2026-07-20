# Attio: List Notes

Retrieves notes from Attio.

```
GET https://connect.mindcloud.co/v1/universal/attio/latest/actions/list-notes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Attio `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/attio/latest/actions/list-notes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/attio/latest/actions/list-notes?${params}`, {
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
| `parentObject` | string | no | Example: `people`. |
| `parentRecordId` | string | no | Example: `891dcbfc-9141-415d-9b2a-2238a6cc012d`. |

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

Through the native Attio API, this operation is `GET /v2/notes` (base URL `https://api.attio.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-notes.md) for the provider-specific parameters and requirements.

