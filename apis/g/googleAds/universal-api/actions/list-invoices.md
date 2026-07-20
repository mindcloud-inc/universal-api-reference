# Google Ads: List Invoices

Retrieves invoices from your Google Ads account.

```
GET https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/list-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Ads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/list-invoices?connectionId=$CONNECTION_ID&customerId=1234567890&billingSetup=customers%2F1234567890%2FbillingSetups%2F1111111111&issueYear=2026&issueMonth=MARCH" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "1234567890",
  "billingSetup": "customers/1234567890/billingSetups/1111111111",
  "issueYear": "2026",
  "issueMonth": "MARCH"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/list-invoices?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | list | yes | Customer ID that owns the Google Ads resources (without dashes). Example: `1234567890`. |
| `billingSetup` | string | yes | Billing setup resource name, for example customers/1234567890/billingSetups/1111111111. Example: `customers/1234567890/billingSetups/1111111111`. |
| `issueYear` | number | yes | Invoice issue year (YYYY). Example: `2026`. |
| `issueMonth` | string | yes | Invoice issue month enum value, for example JANUARY or MARCH. Example: `MARCH`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "invoices": [
        {
          "billingSetup": "string",
          "currencyCode": "string",
          "id": "string",
          "issueDate": "string",
          "pdfUrl": "https://example.com"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `invoices[].billingSetup` | string | Billing setup resource name associated with the invoice. |
| `invoices[].currencyCode` | string | Currency code used for the invoice. |
| `invoices[].id` | string | Invoice identifier. |
| `invoices[].issueDate` | string | Invoice issue date. |
| `invoices[].pdfUrl` | string | PDF download URL for the invoice. |

## Native endpoint

Through the native Google Ads API, this operation is `GET v22/customers/:customerId/invoices` (base URL `https://googleads.googleapis.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-invoices.md) for the provider-specific parameters and requirements.

