# Tumblr: Unlike Post

Removes a like from a Tumblr post.

```
DELETE https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/unlike-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tumblr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/unlike-post?connectionId=$CONNECTION_ID&id=string&reblogKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "reblogKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/unlike-post?${params}`, {
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
| `id` | string | yes | The ID of the post to unlike. |
| `reblogKey` | string | yes | The reblog key for the post. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native Tumblr API, this operation is `POST /v2/user/unlike` (base URL `https://api.tumblr.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unlike-post.md) for the provider-specific parameters and requirements.

