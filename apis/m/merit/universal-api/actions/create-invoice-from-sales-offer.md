# Merit: Create Invoice From Sales Offer



```
POST https://connect.mindcloud.co/v1/universal/merit/latest/actions/create-invoice-from-sales-offer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Merit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/merit/latest/actions/create-invoice-from-sales-offer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "Id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/merit/latest/actions/create-invoice-from-sales-offer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "Id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `Id` | string | yes | Sales offer identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "CustomerId": "string",
      "InvoiceId": "string",
      "InvoiceNo": "string",
      "NewCustomer": "string",
      "RefNo": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CustomerId` | string | Customer identifier linked to the created invoice. |
| `InvoiceId` | string | Created invoice identifier. |
| `InvoiceNo` | string | Created invoice number. |
| `NewCustomer` | string | New customer identifier when Merit created a customer inline. |
| `RefNo` | string | Reference number when present. |

## Native endpoint

Through the native Merit API, this operation is `POST v2/offer2inv` (base URL `https://aktiva.merit.ee/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-invoice-from-sales-offer.md) for the provider-specific parameters and requirements.

