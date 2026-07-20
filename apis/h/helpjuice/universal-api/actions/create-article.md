# Helpjuice: Create Article

Creates a new article in Helpjuice.

```
POST https://connect.mindcloud.co/v1/universal/helpjuice/latest/actions/create-article
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Helpjuice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/helpjuice/latest/actions/create-article" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "categoryId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/helpjuice/latest/actions/create-article', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "categoryId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | Optional article description. |
| `name` | string | yes | The article title. |
| `categoryId` | number | yes | The category ID to assign to the article. |
| `accessibility` | number | no | Optional accessibility value: 1 public, 0 internal, 2 private. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "article": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `article` | object | The created Helpjuice article. |

## Native endpoint

Through the native Helpjuice API, this operation is `POST /articles` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-article.md) for the provider-specific parameters and requirements.

