# 1Shot: List Contract Methods

Retrieves contract method endpoints from 1Shot API.

```
GET https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/list-contract-methods
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 1Shot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/list-contract-methods?connectionId=$CONNECTION_ID&businessId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "businessId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/list-contract-methods?${params}`, {
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
| `name` | string | no |  |
| `status` | string | no |  |
| `contractAddress` | string | no |  |
| `promptId` | string | no |  |
| `methodType` | string | no |  |

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

Through the native 1Shot API, this operation is `GET /business/:businessId/methods` (base URL `https://api.1shotapi.com/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contract-methods.md) for the provider-specific parameters and requirements.

