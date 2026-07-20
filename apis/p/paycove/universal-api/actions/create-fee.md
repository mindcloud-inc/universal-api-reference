# Paycove: Create Fee

Creates a fee for a Paycove deal.

```
POST https://connect.mindcloud.co/v1/universal/paycove/latest/actions/create-fee
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paycove `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/paycove/latest/actions/create-fee" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "crmDealId": "string",
  "label": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/paycove/latest/actions/create-fee', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "crmDealId": "string",
    "label": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `amount` | number | no | Flat fee amount. |
| `crmDealId` | string | yes | The CRM deal ID that owns the fee. |
| `label` | string | yes | The fee label. |
| `percent` | number | no | Percentage fee amount. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fee": {
        "amount": 1,
        "appliesToPaymentFees": true,
        "isTax": true,
        "label": "string",
        "percent": {}
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fee.amount` | number |  |
| `fee.appliesToPaymentFees` | boolean |  |
| `fee.isTax` | boolean |  |
| `fee.label` | string |  |
| `fee.percent` | object |  |
| `message` | string |  |

## Native endpoint

Through the native Paycove API, this operation is `POST deals/:crm_deal_id/fees` (base URL `https://paycove.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-fee.md) for the provider-specific parameters and requirements.

