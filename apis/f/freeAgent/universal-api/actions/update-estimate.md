# FreeAgent: Update Estimate

Updates an existing estimate in FreeAgent.

```
PUT https://connect.mindcloud.co/v1/universal/freeAgent/latest/actions/update-estimate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FreeAgent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/freeAgent/latest/actions/update-estimate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/freeAgent/latest/actions/update-estimate', {
  method: 'PUT',
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
| `id` | string | yes | FreeAgent estimate ID. |
| `estimate` | object | no | Estimate payload. |
| `estimate.status` | string | no | Estimate status. |
| `estimate.estimate_type` | string | no | Estimate type. |
| `estimate.contact` | string | no | Contact for whom the estimate is created. |
| `estimate.project` | string | no | Project being estimated. |
| `estimate.reference` | string | no | Free-text reference. |
| `estimate.dated_on` | date | no | Date of estimate in YYYY-MM-DD format. |
| `estimate.currency` | string | no | Estimate currency. |
| `estimate.notes` | string | no | Additional text. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contact": "string",
      "contact_name": "Ava Chen",
      "created_at": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "dated_on": "2026-05-07T12:00:00.000Z",
      "estimate_type": "string",
      "include_sales_tax_on_total_value": true,
      "involves_sales_tax": true,
      "net_value": "string",
      "notes": "string",
      "project": "string",
      "reference": "string",
      "status": "string",
      "total_value": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact` | string |  |
| `contact_name` | string |  |
| `created_at` | date |  |
| `currency` | string |  |
| `dated_on` | date |  |
| `estimate_type` | string |  |
| `include_sales_tax_on_total_value` | boolean |  |
| `involves_sales_tax` | boolean |  |
| `net_value` | string |  |
| `notes` | string |  |
| `project` | string |  |
| `reference` | string |  |
| `status` | string |  |
| `total_value` | string |  |
| `updated_at` | date |  |
| `url` | string |  |

## Native endpoint

Through the native FreeAgent API, this operation is `PUT /estimates/:id` (base URL `https://api.freeagent.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-estimate.md) for the provider-specific parameters and requirements.

