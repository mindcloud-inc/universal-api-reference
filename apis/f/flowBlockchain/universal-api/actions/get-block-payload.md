# Flow Blockchain: Get Block Payload

Retrieves a block payload from Flow Blockchain.

```
GET https://connect.mindcloud.co/v1/universal/flowBlockchain/latest/actions/get-block-payload
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flow Blockchain `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flowBlockchain/latest/actions/get-block-payload?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flowBlockchain/latest/actions/get-block-payload?${params}`, {
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
| `id` | string | yes | Block ID whose payload should be returned. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "block_seals": [
        {}
      ],
      "collection_guarantees": [
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
| `block_seals` | array<object> | Block seals included in the block payload. |
| `collection_guarantees` | array<object> | Collection guarantees included in the block payload. |

## Native endpoint

Through the native Flow Blockchain API, this operation is `GET /blocks/{id}/payload` (base URL `https://rest-mainnet.onflow.org/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-block-payload.md) for the provider-specific parameters and requirements.

