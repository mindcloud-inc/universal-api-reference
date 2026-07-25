# Amazon Vendor: Submit Purchase Order Acknowledgements



```
POST https://connect.mindcloud.co/v1/universal/amazonVendor/latest/actions/submit-purchase-order-acknowledgements
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amazon Vendor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/amazonVendor/latest/actions/submit-purchase-order-acknowledgements" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "acknowledgements[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/amazonVendor/latest/actions/submit-purchase-order-acknowledgements', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "acknowledgements[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `acknowledgements[]` | array<object> | yes | An array of order acknowledgements to submit. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Amazon Vendor API returns.

## Native endpoint

Through the native Amazon Vendor API, this operation is `POST /vendor/orders/v1/acknowledgements` (base URL `https://sellingpartnerapi-{{credentials.region}}.amazon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-purchase-order-acknowledgements.md) for the provider-specific parameters and requirements.

