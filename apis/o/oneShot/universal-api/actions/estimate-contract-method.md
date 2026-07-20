# 1Shot: Estimate Contract Method

Estimates a contract method transaction in 1Shot API.

```
GET https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/estimate-contract-method
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 1Shot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/estimate-contract-method?connectionId=$CONNECTION_ID&contractMethodId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contractMethodId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/estimate-contract-method?${params}`, {
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
| `contractMethodId` | string | yes |  |
| `params` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "chainId": 1,
      "contractAddress": "string",
      "functionName": "Ava Chen",
      "gasAmount": "string",
      "gasPrice": "string",
      "maxFeePerGas": "string",
      "maxPriorityFeePerGas": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chainId` | number |  |
| `contractAddress` | string |  |
| `functionName` | string |  |
| `gasAmount` | string |  |
| `gasPrice` | string |  |
| `maxFeePerGas` | string |  |
| `maxPriorityFeePerGas` | string |  |

## Native endpoint

Through the native 1Shot API, this operation is `POST /methods/:contractMethodId/estimate` (base URL `https://api.1shotapi.com/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/estimate-contract-method.md) for the provider-specific parameters and requirements.

