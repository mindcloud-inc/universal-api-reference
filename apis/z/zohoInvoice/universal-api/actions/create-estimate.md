# Zoho Invoice: Create Estimate

Creates an estimate in Zoho Invoice.

```
POST https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/create-estimate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Invoice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/create-estimate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationId": "10234695",
  "customerId": "982000000567001",
  "lineItems[]": [
    {}
  ],
  "lineItems[].itemId": "982000000567114",
  "lineItems[].rate": "10.00",
  "lineItems[].quantity": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/create-estimate', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationId": "10234695",
    "customerId": "982000000567001",
    "lineItems[]": [{}],
    "lineItems[].itemId": "982000000567114",
    "lineItems[].rate": "10.00",
    "lineItems[].quantity": "1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationId` | list<string> | yes | ID of the organization header X-com-zoho-invoice-organizationid. Example: `10234695`. |
| `customerId` | string | yes | Customer ID on the estimate. Example: `982000000567001`. |
| `lineItems[]` | array<object> | yes | Line items of the estimate. |
| `lineItems[].itemId` | string | yes | Unique ID of the item. Example: `982000000567114`. |
| `lineItems[].rate` | number | yes | Rate of the line item. Example: `10.00`. |
| `lineItems[].quantity` | number | yes | Quantity of the line item. Example: `1`. |
| `estimateNumber` | string | no | Estimate serial number. |
| `referenceNumber` | string | no | Transaction reference number. |
| `date` | date | no | Date on the estimate. Example: `2026-03-12`. |
| `expiryDate` | date | no | Expiration date of the estimate. Example: `2026-03-31`. |
| `notes` | string | no | Notes added below the estimate. |
| `terms` | string | no | Terms and conditions for the estimate. |
| `lineItems[].name` | string | no | Name of the line item. |
| `lineItems[].description` | string | no | Description of the line item. |
| `lineItems[].unit` | string | no | Unit of measure for the line item. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `send` | boolean | no | Send the estimate to the associated contact persons. |
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

Through the native Zoho Invoice API, this operation is `POST /estimates` (base URL `https://www.zohoapis.com/invoice/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-estimate.md) for the provider-specific parameters and requirements.

