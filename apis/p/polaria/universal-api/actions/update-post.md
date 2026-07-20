# Polaria: Update Post

Updates an existing post in Polaria.

```
PUT https://connect.mindcloud.co/v1/universal/polaria/latest/actions/update-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Polaria `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/polaria/latest/actions/update-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/polaria/latest/actions/update-post', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The ID of the post to update. |
| `title` | string | no |  |
| `content` | string | no |  |
| `status` | string | no |  |
| `cannedResponse` | boolean | no |  |
| `faqCategoryId` | number | no |  |
| `widgets[]` | array<string> | no |  |

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

Through the native Polaria API, this operation is `PUT /faqs/[:id]` (base URL `https://app.polaria.ai/rest/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-post.md) for the provider-specific parameters and requirements.

