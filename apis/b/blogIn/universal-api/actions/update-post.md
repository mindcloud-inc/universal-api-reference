# BlogIn: Update Post

Updates an existing post in BlogIn.

```
PUT https://connect.mindcloud.co/v1/universal/blogIn/latest/actions/update-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BlogIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/blogIn/latest/actions/update-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "title": "string",
  "text": "string",
  "author.id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/blogIn/latest/actions/update-post', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "title": "string",
    "text": "string",
    "author.id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The ID of the post to update. |
| `title` | string | yes | The title of the post. |
| `text` | string | yes | The HTML text of the post. |
| `author.id` | number | yes | The ID of the author of the post. |
| `published` | boolean | no | Whether the post is published. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "approved": true,
      "author": {},
      "categories": [
        {}
      ],
      "comments": 1,
      "comments_disabled": true,
      "date_published": "string",
      "has_published_poll": true,
      "id": 1,
      "important": true,
      "intro_text": "string",
      "pinned": true,
      "post_poll": {},
      "published": true,
      "tags": [
        {}
      ],
      "teams": [
        {}
      ],
      "text": "string",
      "title": "string",
      "visibility_teams": [
        {}
      ],
      "votes_down": 1,
      "votes_up": 1,
      "wiki": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `approved` | boolean |  |
| `author` | object |  |
| `categories` | array<object> |  |
| `comments` | number |  |
| `comments_disabled` | boolean |  |
| `date_published` | string |  |
| `has_published_poll` | boolean |  |
| `id` | number |  |
| `important` | boolean |  |
| `intro_text` | string |  |
| `pinned` | boolean |  |
| `post_poll` | object |  |
| `published` | boolean |  |
| `tags` | array<object> |  |
| `teams` | array<object> |  |
| `text` | string |  |
| `title` | string |  |
| `visibility_teams` | array<object> |  |
| `votes_down` | number |  |
| `votes_up` | number |  |
| `wiki` | boolean |  |

## Native endpoint

Through the native BlogIn API, this operation is `POST /posts/:id` (base URL `https://blogin.co/api/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-post.md) for the provider-specific parameters and requirements.

