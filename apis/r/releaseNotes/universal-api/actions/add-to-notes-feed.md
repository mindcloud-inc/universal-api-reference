# ReleaseNotes: Add to Notes Feed

Creates a new notes feed item in ReleaseNotes.

```
POST https://connect.mindcloud.co/v1/universal/releaseNotes/latest/actions/add-to-notes-feed
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ReleaseNotes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/releaseNotes/latest/actions/add-to-notes-feed" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "11233",
  "notes": "Released a small dashboard performance improvement and filter fix."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/releaseNotes/latest/actions/add-to-notes-feed', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "11233",
    "notes": "Released a small dashboard performance improvement and filter fix."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | The numeric Project ID shown in ReleaseNotes URLs like /manage/project/1234/releases/4321. Example: `11233`. |
| `notes` | string | yes | The note content to append to the project's notes feed. Example: `Released a small dashboard performance improvement and filter fix.`. |
| `title` | string | no | Optional title for the notes feed item. Example: `Dashboard improvement note`. |
| `externalId` | string | no | Optional external identifier for idempotent note appends. Example: `note-123`. |
| `externalLink` | string | no | Optional URL to associate with the notes feed item. Example: `https://example.com/changelog/dashboard-improvements`. |
| `attribution` | string | no | Optional attribution text shown with the notes feed item. Example: `Product Team`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "note": {
        "attribution": "string",
        "createdAt": "string",
        "description": "string",
        "externalId": "string",
        "externalLink": "https://example.com",
        "id": 1,
        "noteAsHtml": "string",
        "noteAsText": "string",
        "source": "string",
        "teamId": 1,
        "title": "string",
        "updatedAt": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `note.attribution` | string |  |
| `note.createdAt` | string |  |
| `note.description` | string |  |
| `note.externalId` | string |  |
| `note.externalLink` | string |  |
| `note.id` | number |  |
| `note.noteAsHtml` | string |  |
| `note.noteAsText` | string |  |
| `note.source` | string |  |
| `note.teamId` | number |  |
| `note.title` | string |  |
| `note.updatedAt` | string |  |

## Native endpoint

Through the native ReleaseNotes API, this operation is `POST /projects/:projectId/notesbucket/append` (base URL `https://api.releasenotes.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-to-notes-feed.md) for the provider-specific parameters and requirements.

