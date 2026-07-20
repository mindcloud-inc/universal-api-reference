# Helpjuice: Update Category

Updates an existing category in Helpjuice.

```
PUT https://connect.mindcloud.co/v1/universal/helpjuice/latest/actions/update-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Helpjuice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/helpjuice/latest/actions/update-category" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/helpjuice/latest/actions/update-category', {
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
| `accessibility` | number | no | The Helpjuice category accessibility. |
| `codename` | string | no | The Helpjuice category codename. |
| `description` | string | no | The Helpjuice category description. |
| `id` | number | yes | The Helpjuice category id. |
| `name` | string | no | The Helpjuice category name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | object | The updated Helpjuice category. |

## Native endpoint

Through the native Helpjuice API, this operation is `PUT /categories/:id` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-category.md) for the provider-specific parameters and requirements.

