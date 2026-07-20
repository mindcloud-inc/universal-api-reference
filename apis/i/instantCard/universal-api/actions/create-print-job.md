# InstantCard: Create Print Job

Creates a new print job in InstantCard.

```
POST https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/create-print-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InstantCard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/create-print-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationId": 1,
  "printJob": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/create-print-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationId": 1,
    "printJob": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationId` | number | yes | Organization ID from your InstantCard account. |
| `printJob` | object | yes | Print job payload including shipping, copies, cards, and either an address_id or one-off address object. |

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

Through the native InstantCard API, this operation is `POST /api/v2/organizations/:organizationId/print_jobs` (base URL `https://core.instantcard.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-print-job.md) for the provider-specific parameters and requirements.

