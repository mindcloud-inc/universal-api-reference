# InstantCard: Get Print Job Charge Details

Retrieves submitted print job charge details from InstantCard.

```
GET https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/get-print-job-charge-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InstantCard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/get-print-job-charge-details?connectionId=$CONNECTION_ID&organizationId=20003827&id=1614262" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "20003827",
  "id": "1614262"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/get-print-job-charge-details?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationId` | number | yes | Organization ID from your InstantCard account. Example: `20003827`. |
| `id` | number | yes | ID of the print job to inspect. Example: `1614262`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "has_balance": true,
      "items": [
        {}
      ],
      "job_total_cost": "string",
      "shipping_cost": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `has_balance` | boolean |  |
| `items` | array<object> |  |
| `job_total_cost` | string |  |
| `shipping_cost` | string |  |

## Native endpoint

Through the native InstantCard API, this operation is `GET /api/v2/organizations/:organizationId/print_jobs/:id/charge_details` (base URL `https://core.instantcard.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-print-job-charge-details.md) for the provider-specific parameters and requirements.

