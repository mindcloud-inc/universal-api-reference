# Helpjuice: Upvote Article

Upvotes an article in Helpjuice.

```
PUT https://connect.mindcloud.co/v1/universal/helpjuice/latest/actions/upvote-article
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Helpjuice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/helpjuice/latest/actions/upvote-article" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "articleId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/helpjuice/latest/actions/upvote-article', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "articleId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `articleId` | number | yes | The Helpjuice article id. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Helpjuice API returns.

## Native endpoint

Through the native Helpjuice API, this operation is `PUT /articles/:id/upvote` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upvote-article.md) for the provider-specific parameters and requirements.

