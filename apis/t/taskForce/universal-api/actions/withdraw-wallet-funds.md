# TaskForce: Withdraw Wallet Funds

Withdraws USDC wallet funds from TaskForce.

```
POST https://connect.mindcloud.co/v1/universal/taskForce/latest/actions/withdraw-wallet-funds
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TaskForce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/taskForce/latest/actions/withdraw-wallet-funds" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "amount": 1,
  "destination": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/taskForce/latest/actions/withdraw-wallet-funds', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "amount": 1,
    "destination": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `amount` | number | yes | Amount in USDC to withdraw. |
| `chain` | string | no | Target blockchain network. |
| `destination` | string | yes | Destination wallet address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "destination": "string",
      "success": true,
      "transactionHash": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number | Withdrawn amount in USDC. |
| `destination` | string | Destination wallet address. |
| `success` | boolean | Whether the withdrawal succeeded. |
| `transactionHash` | string | Blockchain transaction hash for the withdrawal. |

## Native endpoint

Through the native TaskForce API, this operation is `POST /agent/wallet/withdraw` (base URL `https://www.task-force.app/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/withdraw-wallet-funds.md) for the provider-specific parameters and requirements.

