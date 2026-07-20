# Keysender: Add Transaction From Source

Creates a transaction from a source in Keysender.

```
POST https://connect.mindcloud.co/v1/universal/keysender/latest/actions/add-transaction-from-source
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Keysender `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/keysender/latest/actions/add-transaction-from-source" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/keysender/latest/actions/add-transaction-from-source', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `databaseId` | string | no |  |
| `payer` | string | no |  |
| `quantity` | string | no |  |
| `sourceTransactionId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "currency": "string",
      "id": 1,
      "keysenderBuyerEmail": "ava@example.com",
      "name": "Ava Chen",
      "platform": 1,
      "quantity": 1,
      "quantitySent": 1,
      "status": 1,
      "statusAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number | Transaction amount. |
| `currency` | string | Transaction currency. |
| `id` | number | Transaction identifier. |
| `keysenderBuyerEmail` | string | Buyer email for Keysender-originated transactions. |
| `name` | string | Transaction item name. |
| `platform` | number | Transaction platform code. |
| `quantity` | number | Requested quantity. |
| `quantitySent` | number | Quantity already sent. |
| `status` | number | Transaction status code. |
| `statusAt` | date | Status timestamp. |

## Native endpoint

Through the native Keysender API, this operation is `POST /transaction/add` (base URL `https://panel.keysender.co.uk/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-transaction-from-source.md) for the provider-specific parameters and requirements.

