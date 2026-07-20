# Quantum Digital: List Invoices



```
GET https://connect.mindcloud.co/v1/universal/quantumDigital/latest/actions/list-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quantum Digital `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quantumDigital/latest/actions/list-invoices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quantumDigital/latest/actions/list-invoices?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "invoiceDate": "2026-05-07T12:00:00.000Z",
      "invoiceNumber": "string",
      "locationName": "Ava Chen",
      "totalCost": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `invoiceDate` | date | Invoice issue date. |
| `invoiceNumber` | string | Provider invoice number. |
| `locationName` | string | Location name attached to the invoice. |
| `totalCost` | number | Invoice total cost. |

## Native endpoint

Through the native Quantum Digital API, this operation is `GET /devplatform/billing/:dashboardAccountId/invoices` (base URL `https://api.quantumdigital.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-invoices.md) for the provider-specific parameters and requirements.

