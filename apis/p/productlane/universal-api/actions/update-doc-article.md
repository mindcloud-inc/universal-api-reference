# Productlane: Update Doc Article

Updates a help center article in Productlane.

```
PUT https://connect.mindcloud.co/v1/universal/productlane/latest/actions/update-doc-article
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Productlane `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/productlane/latest/actions/update-doc-article" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "95697bff-03d3-4ca1-b079-a153436116ba"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/productlane/latest/actions/update-doc-article', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "95697bff-03d3-4ca1-b079-a153436116ba"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Doc article ID. Example: `95697bff-03d3-4ca1-b079-a153436116ba`. |
| `title` | string | no | Updated article title. Example: `Stage 3 Updated Article`. |
| `content` | string | no | Updated markdown content. Example: `# Updated content`. |
| `summary` | string | no | Updated article summary. Example: `Updated summary`. |
| `published` | boolean | no | Whether the article is published. Default: `true`. |
| `archived` | boolean | no | Whether the article is archived. Default: `false`. |
| `showOnHomePage` | boolean | no | Whether to feature the article on the home page. Default: `true`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Productlane API returns.

## Native endpoint

Through the native Productlane API, this operation is `PATCH /docs/articles/{id}` (base URL `https://productlane.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-doc-article.md) for the provider-specific parameters and requirements.

