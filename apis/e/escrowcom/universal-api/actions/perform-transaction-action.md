# Escrow.com: Perform Transaction Action

Performs a transaction action in Escrow.com.

```
PUT https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/perform-transaction-action
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Escrow.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/perform-transaction-action" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "transactionId": 1,
  "action": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/escrowcom/latest/actions/perform-transaction-action', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "transactionId": 1,
    "action": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `transactionId` | number | yes | The Escrow.com transaction ID. |
| `action` | string | yes | Transaction action to perform, such as agree, ship, receive, accept, reject, cancel, or return. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `actionTo` | string | no | Party role the action is performed for, such as buyer or seller, when supported. |
| `asCustomer` | string | no | Escrow.com customer email to send as the As-Customer header when acting as a partner on behalf of a party. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "closeDate": "2026-05-07T12:00:00.000Z",
      "creationDate": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "description": "string",
      "id": 1,
      "isCancelled": true,
      "items": [
        {}
      ],
      "parties": [
        {}
      ],
      "partnerId": 1,
      "reference": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `closeDate` | date | Transaction close timestamp when available. |
| `creationDate` | date | Transaction creation timestamp. |
| `currency` | string | Transaction currency code. |
| `description` | string | Transaction description. |
| `id` | number | Escrow.com transaction ID. |
| `isCancelled` | boolean | Whether the transaction has been cancelled. |
| `items` | array<object> | Items or milestones included in the transaction. |
| `parties` | array<object> | Parties participating in the transaction. |
| `partnerId` | number | Partner identifier associated with the transaction. |
| `reference` | string | External reference supplied for the transaction. |

## Native endpoint

Through the native Escrow.com API, this operation is `PATCH /transaction/:transaction_id` (base URL `https://api.escrow-sandbox.com/2017-09-01`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/perform-transaction-action.md) for the provider-specific parameters and requirements.

