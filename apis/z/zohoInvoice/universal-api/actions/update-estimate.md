# Zoho Invoice: Update Estimate

Updates an estimate in Zoho Invoice.

```
PUT https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/update-estimate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Invoice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/update-estimate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationId": "10234695",
  "estimateId": "982000000567011"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/update-estimate', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationId": "10234695",
    "estimateId": "982000000567011"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationId` | list<string> | yes | ID of the organization header X-com-zoho-invoice-organizationid. Example: `10234695`. |
| `estimateId` | string | yes | Unique identifier of the estimate. Example: `982000000567011`. |
| `customerId` | string | no | Customer ID on the estimate. |
| `lineItems[]` | array<object> | no | Line items of the estimate. |
| `lineItems[].itemId` | string | no | Unique ID of the item. |
| `lineItems[].rate` | number | no | Rate of the line item. |
| `lineItems[].quantity` | number | no | Quantity of the line item. |
| `estimateNumber` | string | no | Estimate serial number. |
| `referenceNumber` | string | no | Transaction reference number. |
| `date` | date | no | Date on the estimate. Example: `2026-03-12`. |
| `expiryDate` | date | no | Expiration date of the estimate. Example: `2026-03-31`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ignoreAutoNumberGeneration` | boolean | no | Ignore automatic estimate number generation and require a manual estimate number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyName": "Ava Chen",
      "createdTime": "2026-05-07T12:00:00.000Z",
      "currencyCode": "string",
      "customerId": "string",
      "customerName": "Ava Chen",
      "date": "2026-05-07T12:00:00.000Z",
      "estimateId": "string",
      "estimateNumber": "string",
      "expiryDate": "2026-05-07T12:00:00.000Z",
      "lastModifiedTime": "2026-05-07T12:00:00.000Z",
      "referenceNumber": "string",
      "status": "string",
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyName` | string |  |
| `createdTime` | date |  |
| `currencyCode` | string |  |
| `customerId` | string |  |
| `customerName` | string |  |
| `date` | date |  |
| `estimateId` | string |  |
| `estimateNumber` | string |  |
| `expiryDate` | date |  |
| `lastModifiedTime` | date |  |
| `referenceNumber` | string |  |
| `status` | string |  |
| `total` | number |  |

## Native endpoint

Through the native Zoho Invoice API, this operation is `PUT /estimates/:estimate_id` (base URL `https://www.zohoapis.com/invoice/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-estimate.md) for the provider-specific parameters and requirements.

