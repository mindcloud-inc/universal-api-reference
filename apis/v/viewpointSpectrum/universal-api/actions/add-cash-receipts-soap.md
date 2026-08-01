# Viewpoint Spectrum: Add Cash Receipts (SOAP)



```
POST https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/add-cash-receipts-soap
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viewpoint Spectrum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/add-cash-receipts-soap" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/add-cash-receipts-soap', {
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
| `customerCode` | string | no |  |
| `batchCode` | string | no |  |
| `transactionCode` | string | no |  |
| `referenceNumber` | string | no |  |
| `referenceDate` | string | no |  |
| `transactionAmount` | string | no |  |
| `abaNumber` | string | no |  |
| `invoiceNumber` | string | no |  |
| `invoiceType` | string | no |  |
| `paymentAmount` | string | no |  |
| `discountTaken` | string | no |  |
| `costCenterHeader` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Viewpoint Spectrum API returns.

## Native endpoint

Through the native Viewpoint Spectrum API, this operation is `POST /ws/AddCash_Receipts` (base URL `{{credentials.url}}:8482/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-cash-receipts-soap.md) for the provider-specific parameters and requirements.

