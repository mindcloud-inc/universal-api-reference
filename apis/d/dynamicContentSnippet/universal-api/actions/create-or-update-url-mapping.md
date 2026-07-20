# Dynamic Content Snippet: Create or Update URL Mapping

Updates a URL mapping in Dynamic Content Snippet, or creates one if needed.

```
PUT https://connect.mindcloud.co/v1/universal/dynamicContentSnippet/latest/actions/create-or-update-url-mapping
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dynamic Content Snippet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dynamicContentSnippet/latest/actions/create-or-update-url-mapping" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com/page",
  "htmlContent": "<div>Hello World</div>"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dynamicContentSnippet/latest/actions/create-or-update-url-mapping', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com/page",
    "htmlContent": "<div>Hello World</div>"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | URL of the webpage where content will appear. Example: `https://example.com/page`. |
| `htmlContent` | string | yes | HTML content to display at the target URL. ContentSnip allows an empty string to delete content. Example: `<div>Hello World</div>`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dynamic Content Snippet API returns.

## Native endpoint

Through the native Dynamic Content Snippet API, this operation is `POST /api/mappings` (base URL `https://app.contentsnip.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-url-mapping.md) for the provider-specific parameters and requirements.

