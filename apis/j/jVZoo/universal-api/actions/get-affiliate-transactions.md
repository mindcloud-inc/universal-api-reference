# JVZoo: Get Affiliate Transactions

Retrieves your latest affiliate transactions from JVZoo.

```
GET https://connect.mindcloud.co/v1/universal/jVZoo/latest/actions/get-affiliate-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JVZoo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jVZoo/latest/actions/get-affiliate-transactions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jVZoo/latest/actions/get-affiliate-transactions?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `payKey` | string | no | If provided, JVZoo starts after this payKey and does not include it in the results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "affiliateCommission": "string",
      "affiliateCommissionStatus": "string",
      "affiliateId": 1,
      "affiliateName": "Ava Chen",
      "customerEmail": "ava@example.com",
      "date": "2026-05-07T12:00:00.000Z",
      "firstName": "Ava",
      "ip": "string",
      "lastName": "Chen",
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
| `affiliateCommission` | string | Affiliate commission amount. |
| `affiliateCommissionStatus` | string | Affiliate commission payment status. |
| `affiliateId` | number | Affiliate ID. |
| `affiliateName` | string | Affiliate name. |
| `customerEmail` | string | Customer email address. |
| `date` | date | Transaction timestamp. |
| `firstName` | string | Customer first name. |
| `ip` | string | Customer IP address. |
| `lastName` | string | Customer last name. |
| `price` | string | Transaction price. |
| `productId` | number | Product ID. |
| `productName` | string | Product name. |
| `status` | string | Transaction status. |
| `transactionId` | string | JVZoo transaction identifier. |

## Native endpoint

Through the native JVZoo API, this operation is `GET /latest-affiliates-transactions/[:paykey]` (base URL `https://api.jvzoo.com/v2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-affiliate-transactions.md) for the provider-specific parameters and requirements.

