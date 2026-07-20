# Envoice: Get Invoice Details

Retrieves invoice details from Envoice.

```
GET https://connect.mindcloud.co/v1/universal/envoice/latest/actions/get-invoice-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Envoice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/envoice/latest/actions/get-invoice-details?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/envoice/latest/actions/get-invoice-details?${params}`, {
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
| `id` | number | yes | Invoice ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Client": {},
      "Currency": {},
      "Duedate": "2026-05-07T12:00:00.000Z",
      "Id": 1,
      "IssuedOn": "2026-05-07T12:00:00.000Z",
      "Items": [
        {}
      ],
      "Number": "string",
      "PaymentGateways": [
        {}
      ],
      "Status": 1,
      "TotalAmount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Client` | object | Invoice client details. |
| `Currency` | object | Invoice currency details. |
| `Duedate` | date | Invoice due date. |
| `Id` | number | Invoice identifier. |
| `IssuedOn` | date | Invoice issue date. |
| `Items` | array<object> | Invoice line items. |
| `Number` | string | Invoice number. |
| `PaymentGateways` | array<object> | Payment gateways linked to the invoice. |
| `Status` | number | Numeric invoice status. |
| `TotalAmount` | number | Invoice total amount. |

## Native endpoint

Through the native Envoice API, this operation is `GET invoice/details` (base URL `https://www.envoice.in/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-invoice-details.md) for the provider-specific parameters and requirements.

