# Outseta: Change Subscription

Changes an existing subscription in Outseta.

```
PUT https://connect.mindcloud.co/v1/universal/outseta/latest/actions/change-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Outseta `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/outseta/latest/actions/change-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subscriptionUid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/outseta/latest/actions/change-subscription', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subscriptionUid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subscriptionUid` | string | yes |  |
| `plan.uid` | string | no |  |
| `billingRenewalTerm` | number | no |  |
| `account.uid` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Amount": 1,
      "AmountOutstanding": 1,
      "BillingInvoiceStatus": 1,
      "Created": "string",
      "InvoiceDate": "string",
      "Number": 1,
      "Uid": "string",
      "Updated": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Amount` | number |  |
| `AmountOutstanding` | number |  |
| `BillingInvoiceStatus` | number |  |
| `Created` | string |  |
| `InvoiceDate` | string |  |
| `Number` | number |  |
| `Uid` | string |  |
| `Updated` | string |  |

## Native endpoint

Through the native Outseta API, this operation is `PUT /billing/subscriptions/:subscriptionUid/changesubscription` (base URL `https://{{credentials.subdomain}}.outseta.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/change-subscription.md) for the provider-specific parameters and requirements.

