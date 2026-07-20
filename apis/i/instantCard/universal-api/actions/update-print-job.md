# InstantCard: Update Print Job

Updates an existing print job in InstantCard.

```
PUT https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/update-print-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InstantCard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/update-print-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationId": "20003827",
  "id": "1614262"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/update-print-job', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationId": "20003827",
    "id": "1614262"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationId` | number | yes | Organization ID from your InstantCard account. Example: `20003827`. |
| `id` | number | yes | ID of the print job to update. Example: `1614262`. |
| `numberOfCopies` | number | no | Number of copies to print for each card in the print job. Example: `2`. |
| `shippingProviderId` | number | no | Shipping provider ID to use for the print job. Example: `1`. |
| `addressId` | number | no | Saved address ID to use for shipping. Example: `12782`. |

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

Through the native InstantCard API, this operation is `PATCH /api/v2/organizations/:organizationId/print_jobs/:id` (base URL `https://core.instantcard.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-print-job.md) for the provider-specific parameters and requirements.

