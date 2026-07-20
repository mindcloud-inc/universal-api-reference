# OnePageCRM: Create Note

Creates a new note in OnePageCRM.

```
POST https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/create-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OnePageCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/create-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/create-note', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | string | no | ID of the contact the note belongs to. Example: `5ae06ef9d55673108fe8877f`. |
| `text` | string | no | Extra details related to the note. Example: `I met Jane Doe at the ABC conference. She's interested in hearing about XYZ.`. |
| `date` | string | no | Creation date of the note in YYYY-MM-DD format. Example: `2026-03-10`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `linkedDealId` | string | no | Linked deal ID for the note. Example: `5aba31e99007ba0f570c12f7`. |
| `userIdsToNotify[]` | array<string> | no | List of user IDs to notify. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": "string",
      "contactId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "date": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "lastTimelineUpdate": "2026-05-07T12:00:00.000Z",
      "linkedDealId": "https://example.com",
      "linkedDealName": "https://example.com",
      "modifiedAt": "2026-05-07T12:00:00.000Z",
      "text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | string |  |
| `contactId` | string |  |
| `createdAt` | date |  |
| `date` | date |  |
| `id` | string |  |
| `lastTimelineUpdate` | date |  |
| `linkedDealId` | string |  |
| `linkedDealName` | string |  |
| `modifiedAt` | date |  |
| `text` | string |  |

## Native endpoint

Through the native OnePageCRM API, this operation is `POST /notes` (base URL `https://app.onepagecrm.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-note.md) for the provider-specific parameters and requirements.

