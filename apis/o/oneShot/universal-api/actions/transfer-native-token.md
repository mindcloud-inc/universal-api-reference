# 1Shot: Transfer Native Token

Creates a native token transfer from a 1Shot API wallet.

```
POST https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/transfer-native-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 1Shot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/transfer-native-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "walletId": "string",
  "destinationAccountAddress": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/transfer-native-token', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "walletId": "string",
    "destinationAccountAddress": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `walletId` | string | yes |  |
| `destinationAccountAddress` | string | yes |  |
| `transferAmount` | string | no |  |
| `memo` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiCredentialId": "string",
      "apiKey": "string",
      "chainId": 1,
      "completed": 1,
      "contractAddress": "string",
      "contractMethodIds": [
        "string"
      ],
      "created": 1,
      "deleted": true,
      "failureReason": "string",
      "from": "string",
      "functionName": "Ava Chen",
      "gasLimit": "string",
      "gasPrice": "string",
      "gasUsed": "string",
      "id": "string",
      "logs": [
        {
          "args": [
            "string"
          ],
          "name": "Ava Chen",
          "signature": "string",
          "topic": "string"
        }
      ],
      "maxFeePerGas": "string",
      "maxPriorityFeePerGas": "string",
      "memo": "string",
      "name": "Ava Chen",
      "status": "string",
      "to": "string",
      "transactionHash": "string",
      "updated": 1,
      "userId": "string",
      "walletId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiCredentialId` | string |  |
| `apiKey` | string |  |
| `chainId` | number |  |
| `completed` | number |  |
| `contractAddress` | string |  |
| `contractMethodIds[]` | string |  |
| `created` | number |  |
| `deleted` | boolean |  |
| `failureReason` | string |  |
| `from` | string |  |
| `functionName` | string |  |
| `gasLimit` | string |  |
| `gasPrice` | string |  |
| `gasUsed` | string |  |
| `id` | string |  |
| `logs[].args[]` | string |  |
| `logs[].name` | string |  |
| `logs[].signature` | string |  |
| `logs[].topic` | string |  |
| `maxFeePerGas` | string |  |
| `maxPriorityFeePerGas` | string |  |
| `memo` | string |  |
| `name` | string |  |
| `status` | string |  |
| `to` | string |  |
| `transactionHash` | string |  |
| `updated` | number |  |
| `userId` | string |  |
| `walletId` | string |  |

## Native endpoint

Through the native 1Shot API, this operation is `POST /wallets/:walletId/transfer` (base URL `https://api.1shotapi.com/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/transfer-native-token.md) for the provider-specific parameters and requirements.

