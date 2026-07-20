# Hubflo: Create Quote Item for Proposal

Creates a quote item for a Hubflo proposal.

```
POST https://connect.mindcloud.co/v1/universal/hubflo/latest/actions/create-quote-item-for-proposal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hubflo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hubflo/latest/actions/create-quote-item-for-proposal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "proposalId": "string",
  "title": "string",
  "quantity": 1,
  "vat": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hubflo/latest/actions/create-quote-item-for-proposal', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "proposalId": "string",
    "title": "string",
    "quantity": 1,
    "vat": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `proposalId` | string | yes |  |
| `title` | string | yes |  |
| `quantity` | number | yes |  |
| `vat` | number | yes |  |
| `description` | string | no |  |
| `kind` | string | no |  |
| `unitPriceExcludingTax` | string | no |  |
| `unitCostExcludingTax` | string | no |  |
| `discount` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "description": "string",
      "discount_percentage": 1,
      "id": "string",
      "kind": "string",
      "quantity": 1,
      "title": "string",
      "total_excluding_tax": 1,
      "total_including_tax": 1,
      "unit_cost_excluding_tax": 1,
      "unit_price_excluding_tax": 1,
      "vat": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `currency` | string |  |
| `description` | string |  |
| `discount_percentage` | number |  |
| `id` | string |  |
| `kind` | string |  |
| `quantity` | number |  |
| `title` | string |  |
| `total_excluding_tax` | number |  |
| `total_including_tax` | number |  |
| `unit_cost_excluding_tax` | number |  |
| `unit_price_excluding_tax` | number |  |
| `vat` | number |  |

## Native endpoint

Through the native Hubflo API, this operation is `POST /proposals/:proposal_id/line-items` (base URL `https://app.hubflo.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-quote-item-for-proposal.md) for the provider-specific parameters and requirements.

