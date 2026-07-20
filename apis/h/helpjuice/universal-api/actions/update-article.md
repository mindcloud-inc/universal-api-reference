# Helpjuice: Update Article

Updates an existing article in Helpjuice.

```
PUT https://connect.mindcloud.co/v1/universal/helpjuice/latest/actions/update-article
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Helpjuice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/helpjuice/latest/actions/update-article" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/helpjuice/latest/actions/update-article', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | Optional updated article description. |
| `id` | number | yes | The Helpjuice article ID to update. |
| `name` | string | no | Optional updated article title. |
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
| `article` | object | The updated Helpjuice article. |

## Native endpoint

Through the native Helpjuice API, this operation is `PUT /articles/:id` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-article.md) for the provider-specific parameters and requirements.

