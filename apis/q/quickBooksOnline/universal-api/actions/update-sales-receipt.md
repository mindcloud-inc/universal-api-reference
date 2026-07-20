# QuickBooks Online: Update Sales Receipt



```
PUT https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/update-sales-receipt
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuickBooks Online `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/update-sales-receipt" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/update-sales-receipt', {
  method: 'PUT',
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
| `CustomField[].NumberValue` | number | no |  |
| `SyncToken` | string | no |  |
| `Id` | string | no |  |
| `sparse` | boolean | no | Default: `true`. |
| `minorversion` | string | no | Default: `70`. |
| `TrackingNum` | string | no |  |
| `include` | string | no | Default: `enhancedAllCustomFields`. |
| `CustomField[]` | array | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "docNumber": "string",
      "id": "string",
      "line": [
        {}
      ],
      "metaData": {},
      "syncToken": "string",
      "totalAmt": 1,
      "txnDate": "2026-05-07T12:00:00.000Z",
      "vendorRef": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `docNumber` | string |  |
| `id` | string |  |
| `line` | array<object> |  |
| `metaData` | object |  |
| `syncToken` | string |  |
| `totalAmt` | number |  |
| `txnDate` | date |  |
| `vendorRef` | object |  |

## Native endpoint

Through the native QuickBooks Online API, this operation is `POST /salesreceipt` (base URL `https://:quickbooksEnvironment/v3/company/:realmId`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-sales-receipt.md) for the provider-specific parameters and requirements.

