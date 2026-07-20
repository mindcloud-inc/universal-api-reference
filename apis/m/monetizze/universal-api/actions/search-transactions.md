# Monetizze: Search Transactions

Finds transactions in Monetizze by product, email, date, or status.

```
GET https://connect.mindcloud.co/v1/universal/monetizze/latest/actions/search-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Monetizze `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/monetizze/latest/actions/search-transactions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/monetizze/latest/actions/search-transactions?${params}`, {
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
| `product` | number | no | Filter by product code. |
| `transaction` | number | no | Filter by sale code. |
| `email` | string | no | Filter by buyer email. |
| `dateMin` | string | no | Minimum transaction creation date and time in yyyy-mm-dd hh:mm:ss format. |
| `dateMax` | string | no | Maximum transaction creation date and time in yyyy-mm-dd hh:mm:ss format. |
| `endDateMin` | string | no | Minimum finalized sale date and time in yyyy-mm-dd hh:mm:ss format. |
| `endDateMax` | string | no | Maximum finalized sale date and time in yyyy-mm-dd hh:mm:ss format. |
| `status` | number | no | Optional sale status filter values such as 1, 2, 3, 4, 5, or 6. Accepts multiple values as an array. |
| `paymentMethod` | number | no | Optional payment method filter values such as 1, 3, 4, or 8. Accepts multiple values as an array. |
| `page` | number | no | Page number starting at 1. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dados": [
        {}
      ],
      "pages": 1,
      "recordCount": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dados` | array<object> | Transaction rows array; currently empty in runtime evidence. |
| `pages` | number | Total pages reported by Monetizze. |
| `recordCount` | string | Total records count returned by Monetizze. |
| `status` | number | HTTP-style status value returned by Monetizze. |

## Native endpoint

Through the native Monetizze API, this operation is `GET /transactions` (base URL `https://api.monetizze.com.br/2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-transactions.md) for the provider-specific parameters and requirements.

