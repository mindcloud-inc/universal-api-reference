# CompanyCam: Add Comment to Photo



```
POST https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/add-comment-to-photo
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CompanyCam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/add-comment-to-photo" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/add-comment-to-photo', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `comment.content` | string | no | Enter the comment text here. |
| `id` | string | yes | ID of the Photo |
| `comment` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "commentableId": "string",
      "commentableType": "string",
      "content": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creatorId": "string",
      "creatorName": "Ava Chen",
      "creatorType": "string",
      "id": "string",
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `commentableId` | string |  |
| `commentableType` | string |  |
| `content` | string |  |
| `createdAt` | date |  |
| `creatorId` | string |  |
| `creatorName` | string |  |
| `creatorType` | string |  |
| `id` | string |  |
| `status` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native CompanyCam API, this operation is `POST photos/:id/comments` (base URL `https://api.companycam.com/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-comment-to-photo.md) for the provider-specific parameters and requirements.

