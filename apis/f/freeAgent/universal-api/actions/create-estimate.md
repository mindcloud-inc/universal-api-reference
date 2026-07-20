# FreeAgent: Create Estimate

Creates a new estimate in FreeAgent.

```
POST https://connect.mindcloud.co/v1/universal/freeAgent/latest/actions/create-estimate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FreeAgent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/freeAgent/latest/actions/create-estimate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "estimate.status": "string",
  "estimate.estimate_type": "string",
  "estimate.contact": "string",
  "estimate.reference": "string",
  "estimate.dated_on": "2026-05-07T12:00:00.000Z",
  "estimate.currency": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/freeAgent/latest/actions/create-estimate', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "estimate.status": "string",
    "estimate.estimate_type": "string",
    "estimate.contact": "string",
    "estimate.reference": "string",
    "estimate.dated_on": "2026-05-07T12:00:00.000Z",
    "estimate.currency": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `estimate` | object | no | Estimate payload. |
| `estimate.status` | string | yes | Estimate status. |
| `estimate.estimate_type` | string | yes | Estimate type. |
| `estimate.contact` | string | yes | Contact for whom the estimate is created. |
| `estimate.project` | string | no | Project being estimated. |
| `estimate.reference` | string | yes | Free-text reference. |
| `estimate.dated_on` | date | yes | Date of estimate in YYYY-MM-DD format. |
| `estimate.currency` | string | yes | Estimate currency. |
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

Through the native FreeAgent API, this operation is `POST /estimates` (base URL `https://api.freeagent.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-estimate.md) for the provider-specific parameters and requirements.

