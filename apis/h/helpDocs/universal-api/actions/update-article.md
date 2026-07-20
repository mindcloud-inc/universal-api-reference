# HelpDocs: Update Article

Updates an existing article in HelpDocs.

```
PUT https://connect.mindcloud.co/v1/universal/helpDocs/latest/actions/update-article
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HelpDocs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/helpDocs/latest/actions/update-article" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "articleId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/helpDocs/latest/actions/update-article', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "articleId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `articleId` | string | yes | Article ID to update. |
| `body` | string | no | Updated article body HTML. |
| `title` | string | no | Updated article title. |
| `isPublished` | boolean | no | Whether the article is published. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native HelpDocs API returns.

## Native endpoint

Through the native HelpDocs API, this operation is `PATCH /article/:article_id` (base URL `https://api.helpdocs.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-article.md) for the provider-specific parameters and requirements.

