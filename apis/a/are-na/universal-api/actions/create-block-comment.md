# Are.na: Create Block Comment

Creates a new comment on a block in Are.na.

```
POST https://connect.mindcloud.co/v1/universal/are-na/latest/actions/create-block-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Are.na `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/are-na/latest/actions/create-block-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/are-na/latest/actions/create-block-comment', {
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
| `body` | string | no | Comment body. |
| `id` | string | no | Are.na block ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "body": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body` | string |  |
| `created_at` | date |  |
| `id` | number |  |
| `user` | object |  |

## Native endpoint

Through the native Are.na API, this operation is `POST blocks/:id/comments` (base URL `https://api.are.na/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-block-comment.md) for the provider-specific parameters and requirements.

