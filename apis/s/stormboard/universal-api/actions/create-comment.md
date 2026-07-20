# Stormboard: Create Comment

Creates a comment on an idea in Stormboard.

```
POST https://connect.mindcloud.co/v1/universal/stormboard/latest/actions/create-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stormboard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/stormboard/latest/actions/create-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "comment": "string",
  "ideaId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stormboard/latest/actions/create-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "comment": "string",
    "ideaId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `comment` | string | yes | Comment text to post on the idea. |
| `ideaId` | number | yes | Idea ID from a Stormboard idea record. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comment": {
        "comment": "string",
        "id": 1,
        "idea": {
          "id": 1
        },
        "user": {
          "id": 1,
          "name": "Ava Chen"
        }
      },
      "message": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comment` | object |  |
| `comment.comment` | string |  |
| `comment.id` | number |  |
| `comment.idea` | object |  |
| `comment.idea.id` | number |  |
| `comment.user` | object |  |
| `comment.user.id` | number |  |
| `comment.user.name` | string |  |
| `message` | string |  |
| `status` | number |  |

## Native endpoint

Through the native Stormboard API, this operation is `POST /ideas/:idea_id/comments` (base URL `https://api.stormboard.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-comment.md) for the provider-specific parameters and requirements.

