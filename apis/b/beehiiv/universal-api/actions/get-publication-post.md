# Beehiiv: Get Publication Post

Retrieves a publication post from Beehiiv.

```
GET https://connect.mindcloud.co/v1/universal/beehiiv/latest/actions/get-publication-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Beehiiv `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/beehiiv/latest/actions/get-publication-post?connectionId=$CONNECTION_ID&publicationId=string&postId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "publicationId": "string",
  "postId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/beehiiv/latest/actions/get-publication-post?${params}`, {
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
| `publicationId` | string | yes | The prefixed ID of the publication object. |
| `postId` | string | yes | The prefixed ID of the post object. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Beehiiv API returns.

## Native endpoint

Through the native Beehiiv API, this operation is `GET /v2/publications/:publicationId/posts/:postId` (base URL `https://api.beehiiv.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-publication-post.md) for the provider-specific parameters and requirements.

