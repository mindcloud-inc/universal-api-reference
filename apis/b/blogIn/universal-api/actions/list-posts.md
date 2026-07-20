# BlogIn: List Posts

Retrieves all posts from BlogIn.

```
GET https://connect.mindcloud.co/v1/universal/blogIn/latest/actions/list-posts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BlogIn `connectionId` ([setup](../authentication.md)).

This action also supports [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blogIn/latest/actions/list-posts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blogIn/latest/actions/list-posts?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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
      "id": 1,
      "important": true,
      "intro_text": "string",
      "pinned": true,
      "post_poll": {},
      "published": true,
      "thumbnail_image": "string",
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
| `id` | number |  |
| `important` | boolean |  |
| `intro_text` | string |  |
| `pinned` | boolean |  |
| `post_poll` | object |  |
| `published` | boolean |  |
| `thumbnail_image` | string |  |
| `title` | string |  |
| `visibility_teams` | array<object> |  |
| `votes_down` | number |  |
| `votes_up` | number |  |
| `wiki` | boolean |  |

## Native endpoint

Through the native BlogIn API, this operation is `GET /posts` (base URL `https://blogin.co/api/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-posts.md) for the provider-specific parameters and requirements.

