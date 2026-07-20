# Billingo: Get Document

Retrieves a document record from Billingo.

```
GET https://connect.mindcloud.co/v1/universal/billingo/latest/actions/get-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billingo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billingo/latest/actions/get-document?connectionId=$CONNECTION_ID&id=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/billingo/latest/actions/get-document?${params}`, {
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
      "currency": "string",
      "gross_total": 1,
      "id": 1,
      "invoice_date": "2026-05-07T12:00:00.000Z",
      "invoice_number": "string",
      "items": [
        {}
      ],
      "partner": {},
      "payment_status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currency` | string |  |
| `gross_total` | number |  |
| `id` | number |  |
| `invoice_date` | date |  |
| `invoice_number` | string |  |
| `items` | array<object> |  |
| `partner` | object |  |
| `payment_status` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Billingo API, this operation is `GET /documents/:id` (base URL `https://api.billingo.hu/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document.md) for the provider-specific parameters and requirements.

