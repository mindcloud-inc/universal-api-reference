# Charla: Save Article

Saves an article record in Charla.

```
POST https://connect.mindcloud.co/v1/universal/charla/latest/actions/save-article
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Charla `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/charla/latest/actions/save-article" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/charla/latest/actions/save-article', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `article` | string | no | HTML or rich-text article content. |
| `categories[].id` | number | no | Category ID to attach to the article. Add one item per category. |
| `description` | string | no | Short description of the article. |
| `id` | number | no | Provide an existing article ID to update that article. |
| `slug` | string | no | URL slug for the article. |
| `status` | string | no | Status of the article, for example Draft or Published. |
| `title` | string | no | Title of the article. |
| `visibility` | string | no | Visibility of the article, for example Private or Public. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "article": "string",
      "categories": [
        {
          "id": 1,
          "name": "Ava Chen"
        }
      ],
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": 1,
      "slug": "string",
      "status": "string",
      "title": "string",
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `article` | string |  |
| `categories[].id` | number |  |
| `categories[].name` | string |  |
| `created_at` | date |  |
| `description` | string |  |
| `id` | number |  |
| `slug` | string |  |
| `status` | string |  |
| `title` | string |  |
| `visibility` | string |  |

## Native endpoint

Through the native Charla API, this operation is `POST /kb/articles` (base URL `https://api.charla.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/save-article.md) for the provider-specific parameters and requirements.

