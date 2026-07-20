# TravelPerk: Get Invoice

Retrieves an invoice from TravelPerk.

```
GET https://connect.mindcloud.co/v1/universal/travelPerk/latest/actions/get-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TravelPerk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/travelPerk/latest/actions/get-invoice?connectionId=$CONNECTION_ID&invoiceSerialNumber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "invoiceSerialNumber": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/travelPerk/latest/actions/get-invoice?${params}`, {
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
| `invoiceSerialNumber` | string | yes | The invoice serial number to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billing_information": {},
      "billing_period": "string",
      "currency": "string",
      "due_date": "string",
      "from_date": "string",
      "issuing_date": "string",
      "lines": {},
      "mode": "string",
      "pdf": "string",
      "profile_id": "string",
      "profile_name": "Ava Chen",
      "reference": "string",
      "serial_number": "string",
      "status": "string",
      "taxes_summary": [
        {}
      ],
      "to_date": "string",
      "total": "string",
      "travelperk_bank_account": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billing_information` | object |  |
| `billing_period` | string |  |
| `currency` | string |  |
| `due_date` | string |  |
| `from_date` | string |  |
| `issuing_date` | string |  |
| `lines` | object |  |
| `mode` | string |  |
| `pdf` | string |  |
| `profile_id` | string |  |
| `profile_name` | string |  |
| `reference` | string |  |
| `serial_number` | string |  |
| `status` | string |  |
| `taxes_summary` | array<object> |  |
| `to_date` | string |  |
| `total` | string |  |
| `travelperk_bank_account` | object |  |

## Native endpoint

Through the native TravelPerk API, this operation is `GET /invoices/:invoiceSerialNumber` (base URL `https://api.sandbox-travelperk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-invoice.md) for the provider-specific parameters and requirements.

