# 1Shot: Create Contract Method

Creates a new contract method endpoint in 1Shot API.

```
POST https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/create-contract-method
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 1Shot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/create-contract-method" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "businessId": "string",
  "chainId": 1,
  "contractAddress": "string",
  "walletId": "string",
  "name": "Ava Chen",
  "description": "string",
  "functionName": "Ava Chen",
  "stateMutability": "string",
  "inputs": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/create-contract-method', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "businessId": "string",
    "chainId": 1,
    "contractAddress": "string",
    "walletId": "string",
    "name": "Ava Chen",
    "description": "string",
    "functionName": "Ava Chen",
    "stateMutability": "string",
    "inputs": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `businessId` | string | yes |  |
| `chainId` | number | yes |  |
| `contractAddress` | string | yes |  |
| `walletId` | string | yes |  |
| `name` | string | yes |  |
| `description` | string | yes |  |
| `functionName` | string | yes |  |
| `stateMutability` | string | yes |  |
| `inputs` | list<object> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "businessId": "string",
      "callbackUrl": "https://example.com",
      "chainId": 1,
      "contractAddress": "string",
      "created": 1,
      "deleted": true,
      "description": "string",
      "functionName": "Ava Chen",
      "id": "string",
      "inputs": [
        {
          "index": 1,
          "name": "Ava Chen",
          "type": "string"
        }
      ],
      "name": "Ava Chen",
      "promptId": "string",
      "publicKey": "string",
      "stateMutability": "string",
      "updated": 1,
      "walletId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `businessId` | string |  |
| `callbackUrl` | string |  |
| `chainId` | number |  |
| `contractAddress` | string |  |
| `created` | number |  |
| `deleted` | boolean |  |
| `description` | string |  |
| `functionName` | string |  |
| `id` | string |  |
| `inputs[].index` | number |  |
| `inputs[].name` | string |  |
| `inputs[].type` | string |  |
| `name` | string |  |
| `promptId` | string |  |
| `publicKey` | string |  |
| `stateMutability` | string |  |
| `updated` | number |  |
| `walletId` | string |  |

## Native endpoint

Through the native 1Shot API, this operation is `POST /business/:businessId/methods` (base URL `https://api.1shotapi.com/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contract-method.md) for the provider-specific parameters and requirements.

