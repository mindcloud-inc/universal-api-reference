# Moco: Update Comment



```
PUT https://connect.mindcloud.co/v1/universal/moco/latest/actions/update-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moco `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/moco/latest/actions/update-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moco/latest/actions/update-comment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `attachmentContent` | string | no |  |
| `attachmentFilename` | string | no |  |
| `commentableId` | string | no |  |
| `commentableType` | string | no |  |
| `createdAt` | string | no |  |
| `id` | number | yes |  |
| `text` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "commentableId": 1,
      "commentableType": "string",
      "createdAt": "string",
      "id": 1,
      "manual": true,
      "text": "string",
      "updatedAt": "string",
      "user": {
        "firstname": "Ava",
        "id": 1,
        "lastname": "Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `commentableId` | number |  |
| `commentableType` | string |  |
| `createdAt` | string |  |
| `id` | number |  |
| `manual` | boolean |  |
| `text` | string |  |
| `updatedAt` | string |  |
| `user` | object |  |
| `user.firstname` | string |  |
| `user.id` | number |  |
| `user.lastname` | string |  |

## Native endpoint

Through the native Moco API, this operation is `PUT /comments/:id` (base URL `https://{{credentials.domain}}.mocoapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-comment.md) for the provider-specific parameters and requirements.

