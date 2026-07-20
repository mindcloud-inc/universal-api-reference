# Dynamic Content Snippet: Retrieve URL Mappings

Retrieves URL mappings from Dynamic Content Snippet.

```
GET https://connect.mindcloud.co/v1/universal/dynamicContentSnippet/latest/actions/retrieve-url-mappings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dynamic Content Snippet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dynamicContentSnippet/latest/actions/retrieve-url-mappings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dynamicContentSnippet/latest/actions/retrieve-url-mappings?${params}`, {
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
| `url` | string | no | Optional URL filter. ContentSnip docs say it cannot be empty when provided. Example: `https://example.com/page`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "htmlContent": "string",
      "id": "string",
      "isPublished": true,
      "url": "https://example.com",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Mapping creation timestamp in ISO 8601 format. |
| `htmlContent` | string | HTML content for the target URL. |
| `id` | string | ContentSnip mapping identifier. |
| `isPublished` | boolean | Whether the mapping is published. |
| `url` | string | Mapped webpage URL. |
| `userId` | string | ContentSnip user identifier associated with the mapping. |

## Native endpoint

Through the native Dynamic Content Snippet API, this operation is `GET /api/mappings` (base URL `https://app.contentsnip.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-url-mappings.md) for the provider-specific parameters and requirements.

