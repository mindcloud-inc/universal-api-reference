# Stormboard: List Comments

Retrieves comments for an idea in Stormboard.

```
GET https://connect.mindcloud.co/v1/universal/stormboard/latest/actions/list-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stormboard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stormboard/latest/actions/list-comments?connectionId=$CONNECTION_ID&ideaId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ideaId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stormboard/latest/actions/list-comments?${params}`, {
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
| `avatars` | number | no | Set to 1 to include user avatar data, or 0 to skip it. |
| `ideaId` | number | yes | Idea ID from a Stormboard idea record. |
| `order` | string | no | Sort comment order: asc or desc. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comments": [
        {
          "comment": "string",
          "created": "string",
          "id": 1,
          "user": {
            "id": 1,
            "name": "Ava Chen"
          }
        }
      ],
      "length": 1,
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comments` | array<object> |  |
| `comments[].comment` | string |  |
| `comments[].created` | string |  |
| `comments[].id` | number |  |
| `comments[].user` | object |  |
| `comments[].user.id` | number |  |
| `comments[].user.name` | string |  |
| `length` | number |  |
| `status` | number |  |

## Native endpoint

Through the native Stormboard API, this operation is `GET /ideas/:idea_id/comments` (base URL `https://api.stormboard.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-comments.md) for the provider-specific parameters and requirements.

