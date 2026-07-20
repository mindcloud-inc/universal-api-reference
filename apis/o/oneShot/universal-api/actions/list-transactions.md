# 1Shot: List Transactions

Retrieves transaction records from 1Shot API.

```
GET https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/list-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 1Shot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/list-transactions?connectionId=$CONNECTION_ID&businessId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "businessId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/list-transactions?${params}`, {
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
| `businessId` | string | yes | The internal UUID of the business. |
| `chainId` | number | no |  |
| `status` | string | no |  |
| `walletId` | string | no |  |
| `contractMethodId` | string | no |  |
| `apiCredentialId` | string | no |  |
| `userId` | string | no |  |
| `memo` | string | no |  |
| `createdAfter` | date | no |  |
| `createdBefore` | date | no |  |

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

Through the native 1Shot API, this operation is `GET /business/:businessId/transactions` (base URL `https://api.1shotapi.com/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-transactions.md) for the provider-specific parameters and requirements.

