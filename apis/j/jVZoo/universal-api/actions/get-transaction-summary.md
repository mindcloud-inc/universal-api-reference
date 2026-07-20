# JVZoo: Get Transaction Summary

Retrieves a transaction summary from JVZoo.

```
GET https://connect.mindcloud.co/v1/universal/jVZoo/latest/actions/get-transaction-summary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JVZoo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jVZoo/latest/actions/get-transaction-summary?connectionId=$CONNECTION_ID&payKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "payKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jVZoo/latest/actions/get-transaction-summary?${params}`, {
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
| `payKey` | string | yes | The payKey for the transaction you want JVZoo to summarize. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "2026-05-07T12:00:00.000Z",
      "firstName": "Ava",
      "lastName": "Chen",
      "paypalEmail": "ava@example.com",
      "price": "string",
      "productId": 1,
      "productName": "Ava Chen",
      "status": "string",
      "transactionId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | date | Transaction timestamp. |
| `firstName` | string | Customer first name. |
| `lastName` | string | Customer last name. |
| `paypalEmail` | string | PayPal email address. |
| `price` | string | Transaction price. |
| `productId` | number | Product ID. |
| `productName` | string | Product name. |
| `status` | string | Transaction status. |
| `transactionId` | string | JVZoo transaction identifier. |

## Native endpoint

Through the native JVZoo API, this operation is `GET /transactions/summaries/:paykey` (base URL `https://api.jvzoo.com/v2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transaction-summary.md) for the provider-specific parameters and requirements.

