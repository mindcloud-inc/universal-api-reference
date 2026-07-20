# Chainstream: Get Latest Block

Retrieves the latest blockchain block from Chainstream.

```
GET https://connect.mindcloud.co/v1/universal/chainstream/latest/actions/get-latest-block
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chainstream `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chainstream/latest/actions/get-latest-block?connectionId=$CONNECTION_ID&chain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chain": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chainstream/latest/actions/get-latest-block?${params}`, {
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
| `chain` | string | yes | A chain name listed in supported networks. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "blockhash": "string",
      "lastValidBlockHeight": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blockhash` | string |  |
| `lastValidBlockHeight` | number |  |

## Native endpoint

Through the native Chainstream API, this operation is `GET /v2/blockchain/:chain/latest_block` (base URL `https://api.chainstream.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-latest-block.md) for the provider-specific parameters and requirements.

