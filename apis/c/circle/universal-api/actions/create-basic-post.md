# Circle: Create Basic Post

Creates a new basic post in Circle.

```
POST https://connect.mindcloud.co/v1/universal/circle/latest/actions/create-basic-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Circle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/circle/latest/actions/create-basic-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "spaceId": 1,
  "name": "Ava Chen",
  "body": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/circle/latest/actions/create-basic-post', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "spaceId": 1,
    "name": "Ava Chen",
    "body": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `spaceId` | list<number> | yes | Space ID for the post |
| `name` | string | yes | Post title |
| `body` | string | yes | Post body content |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "post": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `post` | object |  |

## Native endpoint

Through the native Circle API, this operation is `POST /api/admin/v2/posts` (base URL `https://{{credentials.subdomain}}.circle.so`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-basic-post.md) for the provider-specific parameters and requirements.

