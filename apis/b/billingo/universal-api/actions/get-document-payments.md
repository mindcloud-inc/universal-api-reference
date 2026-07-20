# Billingo: Get Document Payments

Retrieves payment history for a document in Billingo.

```
GET https://connect.mindcloud.co/v1/universal/billingo/latest/actions/get-document-payments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billingo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billingo/latest/actions/get-document-payments?connectionId=$CONNECTION_ID&id=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/billingo/latest/actions/get-document-payments?${params}`, {
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
| `id` | number | yes | Billingo document ID from the path. Default: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "conversion_rate": 1,
      "date": "2026-05-07T12:00:00.000Z",
      "payment_method": "string",
      "price": 1,
      "voucher_number": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `conversion_rate` | number |  |
| `date` | date |  |
| `payment_method` | string |  |
| `price` | number |  |
| `voucher_number` | string |  |

## Native endpoint

Through the native Billingo API, this operation is `GET /documents/:id/payments` (base URL `https://api.billingo.hu/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document-payments.md) for the provider-specific parameters and requirements.

