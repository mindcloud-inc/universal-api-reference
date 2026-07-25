# Rillion Prime Pay: Create Payment Supplier Grouping



```
POST https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/create-payment-supplier-grouping
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime Pay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/create-payment-supplier-grouping" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "supplierPaymentGrouping": "Bundle"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/create-payment-supplier-grouping', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "supplierPaymentGrouping": "Bundle"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `xCorrelationId` | string | no |  |
| `supplierPaymentGrouping` | list<string> | yes | Payment grouping option applied to all suppliers One of: `Bundle`, `SendIndividually`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rillion Prime Pay API returns.

## Native endpoint

Through the native Rillion Prime Pay API, this operation is `POST /payment/suppliers/grouping` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-payment-supplier-grouping.md) for the provider-specific parameters and requirements.

