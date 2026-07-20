# Polaria: List Posts

Retrieves posts from Polaria.

```
GET https://connect.mindcloud.co/v1/universal/polaria/latest/actions/list-posts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Polaria `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/polaria/latest/actions/list-posts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/polaria/latest/actions/list-posts?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "externalId": "string",
      "faqCategoryId": 1,
      "format": "string",
      "id": 1,
      "slug": "string",
      "status": "string",
      "title": "string",
      "translations": [
        {}
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "widgets": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `externalId` | string |  |
| `faqCategoryId` | number |  |
| `format` | string |  |
| `id` | number |  |
| `slug` | string |  |
| `status` | string |  |
| `title` | string |  |
| `translations` | array<object> |  |
| `updatedAt` | date |  |
| `widgets` | array<string> |  |

## Native endpoint

Through the native Polaria API, this operation is `GET /faqs` (base URL `https://app.polaria.ai/rest/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-posts.md) for the provider-specific parameters and requirements.

