# Sage Intacct: Create Invoice



```
POST https://connect.mindcloud.co/v1/universal/intacct/latest/actions/create-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sage Intacct `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/intacct/latest/actions/create-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/intacct/latest/actions/create-invoice', {
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
| `invoiceItems[].amount` | number | no |  |
| `invoiceItems[].glAccountNo` | string | no |  |
| `dateCreated` | string | no | MM/DD/YYYY |
| `invoiceItems[]` | array | no |  |
| `invoiceItems[].locationId` | number | no |  |
| `invoiceItems[].divisionId` | number | no |  |
| `invoiceNumber` | string | no |  |
| `invoiceItems[].accountLabel` | string | no |  |
| `locationId` | string | no |  |
| `divisionId` | string | no |  |
| `invoiceItems[].memo` | string | no |  |
| `externalId` | string | no |  |
| `dateDue` | string | no | MM/DD/YYYY |
| `description` | string | no |  |
| `datePosted` | string | no |  |
| `poNumber` | string | no |  |
| `customFields[]` | array | no | [{ customfieldname:"..." customfieldvalue:"testing" }] |
| `supdocId` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Sage Intacct API returns.

## Native endpoint

Through the native Sage Intacct API, this operation is `POST` (base URL `https://api.intacct.com/ia/xml/xmlgw.phtml`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-invoice.md) for the provider-specific parameters and requirements.

