# Solana: Get Genesis Hash

Retrieves the genesis hash from Solana.

```
GET https://connect.mindcloud.co/v1/universal/solana/latest/actions/get-genesis-hash
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Solana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/solana/latest/actions/get-genesis-hash?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/solana/latest/actions/get-genesis-hash?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "jsonrpc": "string",
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `jsonrpc` | string |  |
| `result` | string |  |

## Native endpoint

Through the native Solana API, this operation is `POST /` (base URL `https://api.mainnet-beta.solana.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-genesis-hash.md) for the provider-specific parameters and requirements.

