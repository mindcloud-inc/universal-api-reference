# Toofr: Purchase Marketplace List

Purchases a marketplace email list in Toofr.

```
POST https://connect.mindcloud.co/v1/universal/toofr/latest/actions/purchase-marketplace-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toofr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/toofr/latest/actions/purchase-marketplace-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/toofr/latest/actions/purchase-marketplace-list', {
  method: 'POST',
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
| `id` | string | yes | Marketplace email list ID to purchase. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "file_type": "string",
      "id": "string",
      "list_records_count": 1,
      "name": "Ava Chen",
      "records_count_in": 1,
      "records_count_processed": 1,
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `description` | string |  |
| `file_type` | string |  |
| `id` | string |  |
| `list_records_count` | number |  |
| `name` | string |  |
| `records_count_in` | number |  |
| `records_count_processed` | number |  |
| `state` | string |  |

## Native endpoint

Through the native Toofr API, this operation is `POST /lists/:id/purchase` (base URL `https://www.findemails.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/purchase-marketplace-list.md) for the provider-specific parameters and requirements.

