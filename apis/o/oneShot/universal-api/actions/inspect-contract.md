# 1Shot: Inspect Contract

Retrieves contract details from 1Shot API.

```
GET https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/inspect-contract
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 1Shot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/inspect-contract?connectionId=$CONNECTION_ID&chainId=string&contractAddress=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chainId": "string",
  "contractAddress": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/inspect-contract?${params}`, {
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
| `chainId` | string | yes | The chain identifier. |
| `contractAddress` | string | yes | The contract address to inspect. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "eip7702ImplementationAddress": "string",
      "isContract": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `eip7702ImplementationAddress` | string |  |
| `isContract` | boolean |  |

## Native endpoint

Through the native 1Shot API, this operation is `GET /chains/:chainId/contracts/:contractAddress` (base URL `https://api.1shotapi.com/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/inspect-contract.md) for the provider-specific parameters and requirements.

