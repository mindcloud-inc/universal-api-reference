# Shortcut: Create Story Comment



```
POST https://connect.mindcloud.co/v1/universal/shortcut/latest/actions/create-story-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shortcut `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shortcut/latest/actions/create-story-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "storyPublicId": 1,
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shortcut/latest/actions/create-story-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "storyPublicId": 1,
    "text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `storyPublicId` | number | yes |  |
| `text` | string | yes |  |
| `authorId` | string | no |  |
| `externalId` | string | no |  |
| `parentId` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authorId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deleted": true,
      "entityType": "string",
      "id": 1,
      "linkedToSlack": true,
      "position": 1,
      "storyId": 1,
      "text": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authorId` | string |  |
| `createdAt` | date |  |
| `deleted` | boolean |  |
| `entityType` | string |  |
| `id` | number |  |
| `linkedToSlack` | boolean |  |
| `position` | number |  |
| `storyId` | number |  |
| `text` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Shortcut API, this operation is `POST /stories/:storyPublicId/comments` (base URL `https://api.app.shortcut.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-story-comment.md) for the provider-specific parameters and requirements.

