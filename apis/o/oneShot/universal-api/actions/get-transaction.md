# 1Shot: Get Transaction

Retrieves transaction details from 1Shot API.

```
GET https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/get-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 1Shot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/get-transaction?connectionId=$CONNECTION_ID&transactionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "transactionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/get-transaction?${params}`, {
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
| `transactionId` | string | yes | The internal UUID of the transaction. |

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

Through the native 1Shot API, this operation is `GET /transactions/:transactionId` (base URL `https://api.1shotapi.com/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transaction.md) for the provider-specific parameters and requirements.

