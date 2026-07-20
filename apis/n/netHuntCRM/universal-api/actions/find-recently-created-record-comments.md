# NetHunt CRM: Find Recently Created Record Comments

Finds recently created record comments in NetHunt CRM.

```
GET https://connect.mindcloud.co/v1/universal/netHuntCRM/latest/actions/find-recently-created-record-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetHunt CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netHuntCRM/latest/actions/find-recently-created-record-comments?connectionId=$CONNECTION_ID&folderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "folderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netHuntCRM/latest/actions/find-recently-created-record-comments?${params}`, {
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
| `folderId` | string | yes | Folder ID to watch for new comments. |
| `since` | string | no | Only comments created after this ISO timestamp are returned. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "commentId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "recordId": "string",
      "text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `commentId` | string |  |
| `createdAt` | date |  |
| `id` | string |  |
| `recordId` | string |  |
| `text` | string |  |

## Native endpoint

Through the native NetHunt CRM API, this operation is `GET /triggers/new-comment/:folderId` (base URL `https://nethunt.com/api/v1/zapier`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-recently-created-record-comments.md) for the provider-specific parameters and requirements.

