# Stockpilot: Create Category

Creates a new category in Stockpilot.

```
POST https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/create-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stockpilot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/create-category" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Audio"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/create-category', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Audio"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Category name Example: `Audio`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "product_category": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | Stockpilot category ID |
| `product_category` | string | Category name |

## Native endpoint

Through the native Stockpilot API, this operation is `POST /categories/create` (base URL `https://api.stockpilot.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-category.md) for the provider-specific parameters and requirements.

