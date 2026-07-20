# Soundee: Get Transaction

Retrieves a transaction record from Soundee.

```
GET https://connect.mindcloud.co/v1/universal/soundee/latest/actions/get-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Soundee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/soundee/latest/actions/get-transaction?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/soundee/latest/actions/get-transaction?${params}`, {
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
| `id` | string | yes | The transaction ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addressDetails": {},
      "created": 1,
      "currency": {},
      "customer": {},
      "fee": "string",
      "gross": 1,
      "id": 1,
      "invoice": {},
      "ip": "string",
      "items": [
        {}
      ],
      "merchant": {},
      "net": 1,
      "parameters": {},
      "parentTransactionId": "string",
      "paymentSource": {},
      "paymentStatus": "string",
      "receiptUrl": "https://example.com",
      "store": {},
      "tax": 1,
      "taxRate": 1,
      "transactionId": "string",
      "transactionType": "string",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addressDetails` | object |  |
| `created` | number |  |
| `currency` | object |  |
| `customer` | object |  |
| `fee` | string |  |
| `gross` | number |  |
| `id` | number |  |
| `invoice` | object |  |
| `ip` | string |  |
| `items` | array<object> |  |
| `merchant` | object |  |
| `net` | number |  |
| `parameters` | object |  |
| `parentTransactionId` | string |  |
| `paymentSource` | object |  |
| `paymentStatus` | string |  |
| `receiptUrl` | string |  |
| `store` | object |  |
| `tax` | number |  |
| `taxRate` | number |  |
| `transactionId` | string |  |
| `transactionType` | string |  |
| `userId` | number |  |

## Native endpoint

Through the native Soundee API, this operation is `GET /transactions/:id` (base URL `https://api.soundee.com/me`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transaction.md) for the provider-specific parameters and requirements.

