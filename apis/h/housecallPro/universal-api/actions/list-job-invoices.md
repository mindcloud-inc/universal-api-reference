# Housecall Pro: List Job Invoices



```
GET https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/list-job-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Housecall Pro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/list-job-invoices?connectionId=$CONNECTION_ID&jobId=job_b5238dca70b74f70acd0ee47b56bb467" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "job_b5238dca70b74f70acd0ee47b56bb467"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/list-job-invoices?${params}`, {
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
| `jobId` | string | yes | The job whose invoices should be listed. Example: `job_b5238dca70b74f70acd0ee47b56bb467`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "discounts": [
        {}
      ],
      "displayDueConcept": "string",
      "dueAmount": 1,
      "dueAt": "string",
      "dueConcept": "string",
      "id": "string",
      "invoiceDate": "string",
      "invoiceNumber": "string",
      "items": [
        {}
      ],
      "paidAt": "string",
      "payments": [
        {}
      ],
      "sentAt": "string",
      "serviceDate": "string",
      "status": "string",
      "subtotal": 1,
      "taxes": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number | Invoice total amount. |
| `discounts` | array<object> | Invoice discounts. |
| `displayDueConcept` | string | Human-readable due concept. |
| `dueAmount` | number | Outstanding invoice balance. |
| `dueAt` | string | Invoice due timestamp. |
| `dueConcept` | string | Provider due concept token. |
| `id` | string | Invoice UUID. |
| `invoiceDate` | string | Invoice date. |
| `invoiceNumber` | string | Invoice number. |
| `items` | array<object> | Invoice items. |
| `paidAt` | string | Paid timestamp. |
| `payments` | array<object> | Invoice payments. |
| `sentAt` | string | Sent timestamp. |
| `serviceDate` | string | Service date. |
| `status` | string | Invoice status. |
| `subtotal` | number | Invoice subtotal amount. |
| `taxes` | array<object> | Invoice taxes. |

## Native endpoint

Through the native Housecall Pro API, this operation is `GET /jobs/:job_id/invoices` (base URL `https://api.housecallpro.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-job-invoices.md) for the provider-specific parameters and requirements.

