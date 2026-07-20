# Discourse: Like Post

Adds a like to a Discourse post.

```
PUT https://connect.mindcloud.co/v1/universal/discourse/latest/actions/like-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discourse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/discourse/latest/actions/like-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/discourse/latest/actions/like-post', {
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
| `id` | number | yes | Post id to like. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "post_number": 1,
      "post_url": "https://example.com",
      "topic_id": 1,
      "topic_slug": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `post_number` | number |  |
| `post_url` | string |  |
| `topic_id` | number |  |
| `topic_slug` | string |  |

## Native endpoint

Through the native Discourse API, this operation is `POST /post_actions.json` (base URL `https://mindcloud.discourse.group`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/like-post.md) for the provider-specific parameters and requirements.

