# Conveyor: Create Review



```
POST https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/create-review
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Conveyor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/create-review" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "vendorName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/create-review', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "vendorName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Reviewer email address. |
| `iterationVmId` | string | no | Iteration vendor-management identifier. |
| `questionGroupId` | string | no | Question group identifier. |
| `vendorVmId` | string | no | Vendor-management vendor identifier. |
| `vendorName` | string | yes | Vendor name for the review. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_type": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "vendor_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_type` | string |  |
| `created_at` | date |  |
| `id` | string |  |
| `updated_at` | date |  |
| `vendor_id` | string |  |

## Native endpoint

Through the native Conveyor API, this operation is `POST /v2/reviews` (base URL `https://api.conveyor.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-review.md) for the provider-specific parameters and requirements.

