# Flow Blockchain: Get Account

Retrieves an account from Flow Blockchain.

```
GET https://connect.mindcloud.co/v1/universal/flowBlockchain/latest/actions/get-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flow Blockchain `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flowBlockchain/latest/actions/get-account?connectionId=$CONNECTION_ID&address=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "address": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flowBlockchain/latest/actions/get-account?${params}`, {
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
| `address` | string | yes | Flow account address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_expandable": {},
      "_links": {},
      "address": "string",
      "balance": "string",
      "contracts": {},
      "keys": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_expandable` | object | Expandable Flow API resource links. |
| `_links` | object | Flow API resource links. |
| `address` | string | Flow account address. |
| `balance` | string | Flow account balance. |
| `contracts` | object | Deployed account contracts. |
| `keys` | array<object> | Account keys. |

## Native endpoint

Through the native Flow Blockchain API, this operation is `GET /accounts/{address}` (base URL `https://rest-mainnet.onflow.org/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account.md) for the provider-specific parameters and requirements.

