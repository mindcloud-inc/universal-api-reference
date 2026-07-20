# Pinch Payments: List Processed Payments

Retrieves processed payments from Pinch Payments.

```
GET https://connect.mindcloud.co/v1/universal/pinchPayments/latest/actions/list-processed-payments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinch Payments `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pinchPayments/latest/actions/list-processed-payments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pinchPayments/latest/actions/list-processed-payments?${params}`, {
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
| `endDate` | date | no |  |
| `filter` | string | no |  |
| `startDate` | date | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "id": "string"
        }
      ],
      "page": 1,
      "pageSize": 1,
      "totalItems": 1,
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `data[].id` | string |  |
| `page` | number |  |
| `pageSize` | number |  |
| `totalItems` | number |  |
| `totalPages` | number |  |

## Native endpoint

Through the native Pinch Payments API, this operation is `GET /payments/processed` (base URL `https://api.getpinch.com.au/live`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-processed-payments.md) for the provider-specific parameters and requirements.

