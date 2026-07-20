# InstantCard: Add Cards To Print Job

Updates an existing print job in InstantCard by adding cards.

```
PUT https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/add-cards-to-print-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InstantCard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/add-cards-to-print-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationId": 1,
  "id": 1,
  "cardIds": "3096409,3145927"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/add-cards-to-print-job', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationId": 1,
    "id": 1,
    "cardIds": "3096409,3145927"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationId` | number | yes | Organization ID from your InstantCard account. |
| `id` | number | yes | ID of the print job to update. |
| `cardIds` | string | yes | Array string of card IDs to add, exactly as InstantCard expects, for example [3096409,3145927]. Example: `3096409,3145927`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {},
      "address_id": 1,
      "created_at": "string",
      "extract": {},
      "id": 1,
      "list_users": [
        {}
      ],
      "organization": {},
      "status": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | object |  |
| `address_id` | number |  |
| `created_at` | string |  |
| `extract` | object |  |
| `id` | number |  |
| `list_users` | array<object> |  |
| `organization` | object |  |
| `status` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native InstantCard API, this operation is `POST /api/v2/organizations/:organizationId/print_jobs/:id/add_cards` (base URL `https://core.instantcard.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-cards-to-print-job.md) for the provider-specific parameters and requirements.

