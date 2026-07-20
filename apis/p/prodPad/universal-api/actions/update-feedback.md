# ProdPad: Update Feedback

Updates existing feedback in ProdPad.

```
PUT https://connect.mindcloud.co/v1/universal/prodPad/latest/actions/update-feedback
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProdPad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/prodPad/latest/actions/update-feedback" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/prodPad/latest/actions/update-feedback', {
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
| `id` | number | yes |  |
| `feedback` | string | no |  |
| `state` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "added_by": {
        "display_name": "Ava Chen",
        "id": 1,
        "username": "Ava Chen"
      },
      "created_at": "2026-05-07T12:00:00.000Z",
      "customer": {
        "about": "string",
        "created_at": "2026-05-07T12:00:00.000Z",
        "email": "ava@example.com",
        "id": 1,
        "name": "Ava Chen",
        "updated_at": "2026-05-07T12:00:00.000Z"
      },
      "feedback": "string",
      "id": 1,
      "source": "string",
      "state": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `added_by.display_name` | string |  |
| `added_by.id` | number |  |
| `added_by.username` | string |  |
| `created_at` | date |  |
| `customer.about` | string |  |
| `customer.created_at` | date |  |
| `customer.email` | string |  |
| `customer.id` | number |  |
| `customer.name` | string |  |
| `customer.updated_at` | date |  |
| `feedback` | string |  |
| `id` | number |  |
| `source` | string |  |
| `state` | string |  |
| `updated_at` | date |  |
| `uuid` | string |  |

## Native endpoint

Through the native ProdPad API, this operation is `PUT /feedbacks/:id` (base URL `https://api.prodpad.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-feedback.md) for the provider-specific parameters and requirements.

