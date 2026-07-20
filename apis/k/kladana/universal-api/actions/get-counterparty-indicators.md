# Kladana: Get Counterparty Indicators

Retrieves counterparty indicators report from Kladana.

```
GET https://connect.mindcloud.co/v1/universal/kladana/latest/actions/get-counterparty-indicators
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kladana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kladana/latest/actions/get-counterparty-indicators?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kladana/latest/actions/get-counterparty-indicators?${params}`, {
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
      "balance": 1,
      "code": "string",
      "counterparty": {},
      "email": "ava@example.com",
      "firstDemandDate": "2026-05-07T12:00:00.000Z",
      "lastDemandDate": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "paymentsAmount": 1,
      "phone": "string",
      "profit": 1,
      "returnsAmount": 1,
      "salesAmount": 1,
      "shippedAmount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balance` | number | Counterparty balance. |
| `code` | string | Internal code. |
| `counterparty` | object | Counterparty reference. |
| `email` | string | Email address. |
| `firstDemandDate` | date | First shipment date. |
| `lastDemandDate` | date | Last shipment date. |
| `name` | string | Counterparty name. |
| `paymentsAmount` | number | Payments amount. |
| `phone` | string | Phone number. |
| `profit` | number | Profit amount. |
| `returnsAmount` | number | Returns amount. |
| `salesAmount` | number | Sales amount. |
| `shippedAmount` | number | Shipped amount. |

## Native endpoint

Through the native Kladana API, this operation is `GET /report/counterparty` (base URL `https://api.kladana.com/api/remap/1.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-counterparty-indicators.md) for the provider-specific parameters and requirements.

