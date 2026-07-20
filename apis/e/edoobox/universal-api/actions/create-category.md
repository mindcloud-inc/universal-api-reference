# Edoobox: Create Category

Creates a new category in Edoobox.

```
POST https://connect.mindcloud.co/v1/universal/edoobox/latest/actions/create-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Edoobox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/edoobox/latest/actions/create-category" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "design": "string",
  "type": "folder"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/edoobox/latest/actions/create-category', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "design": "string",
    "type": "folder"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Category name. |
| `design` | string | yes | edoobox design ID for the category. |
| `category` | string | no | Parent edoobox category ID. |
| `type` | string | yes | edoobox category type. Default: `folder`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "insert": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `insert` | boolean |  |

## Native endpoint

Through the native Edoobox API, this operation is `POST /category` (base URL `https://app2.edoobox.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-category.md) for the provider-specific parameters and requirements.

