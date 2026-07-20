# Voog: Update Article

Updates an existing article in the current Voog site.

```
PUT https://connect.mindcloud.co/v1/universal/voog/latest/actions/update-article
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/voog/latest/actions/update-article" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "articleId": 1,
  "autosavedTitle": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/voog/latest/actions/update-article', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "articleId": 1,
    "autosavedTitle": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `articleId` | number | yes | Numeric article ID. |
| `autosavedTitle` | string | yes | Updated draft article title. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Voog API returns.

## Native endpoint

Through the native Voog API, this operation is `PUT /articles/:articleId` (base URL `{{credentials.siteUrl}}/admin/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-article.md) for the provider-specific parameters and requirements.

