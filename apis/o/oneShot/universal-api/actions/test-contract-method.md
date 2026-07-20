# 1Shot: Test Contract Method

Tests a contract method endpoint in 1Shot API.

```
GET https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/test-contract-method
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 1Shot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/test-contract-method?connectionId=$CONNECTION_ID&contractMethodId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contractMethodId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/test-contract-method?${params}`, {
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
      "error": {
        "code": "string",
        "decodedData": {
          "args": [
            "string"
          ],
          "name": "Ava Chen",
          "selector": "string"
        },
        "message": "string",
        "reason": "string",
        "revert": {
          "name": "Ava Chen",
          "signature": "string"
        },
        "transaction": {
          "data": "string",
          "from": "string",
          "to": "string"
        }
      },
      "result": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error.code` | string |  |
| `error.decodedData.args[]` | string |  |
| `error.decodedData.name` | string |  |
| `error.decodedData.selector` | string |  |
| `error.message` | string |  |
| `error.reason` | string |  |
| `error.revert.name` | string |  |
| `error.revert.signature` | string |  |
| `error.transaction.data` | string |  |
| `error.transaction.from` | string |  |
| `error.transaction.to` | string |  |
| `result` | object |  |
| `success` | boolean |  |

## Native endpoint

Through the native 1Shot API, this operation is `POST /methods/:contractMethodId/test` (base URL `https://api.1shotapi.com/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/test-contract-method.md) for the provider-specific parameters and requirements.

