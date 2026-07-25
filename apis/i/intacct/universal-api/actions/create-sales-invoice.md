# Sage Intacct: Create Sales Invoice



```
POST https://connect.mindcloud.co/v1/universal/intacct/latest/actions/create-sales-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sage Intacct `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/intacct/latest/actions/create-sales-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/intacct/latest/actions/create-sales-invoice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | string | no |  |
| `customFields[].name` | string | no |  |
| `invoiceItems[].itemId` | string | no |  |
| `customFields[].value` | string | no |  |
| `dateCreated` | string | no |  |
| `invoiceItems[].price` | number | no |  |
| `invoiceItems[]` | array | no |  |
| `documentNumber` | string | no |  |
| `invoiceItems[].locationId` | string | no |  |
| `invoiceItems[].divisionId` | string | no |  |
| `invoiceItems[].quantity` | number | no | Default: `1`. |
| `message` | string | no |  |
| `entityID` | string | no |  |
| `invoiceItems[].description` | string | no |  |
| `state` | string | no | Draft \| Pending \| Closed Default: `Draft`. |
| `referenceNumber` | string | no |  |
| `customFields[]` | array<object> | no |  |
| `customerPONumber` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Sage Intacct API returns.

## Native endpoint

Through the native Sage Intacct API, this operation is `POST` (base URL `https://api.intacct.com/ia/xml/xmlgw.phtml`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sales-invoice.md) for the provider-specific parameters and requirements.

