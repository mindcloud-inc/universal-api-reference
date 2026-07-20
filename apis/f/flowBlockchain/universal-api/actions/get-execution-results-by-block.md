# Flow Blockchain: Get Execution Results by Block

Retrieves execution results from Flow Blockchain by block.

```
GET https://connect.mindcloud.co/v1/universal/flowBlockchain/latest/actions/get-execution-results-by-block
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flow Blockchain `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flowBlockchain/latest/actions/get-execution-results-by-block?connectionId=$CONNECTION_ID&blockId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "blockId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flowBlockchain/latest/actions/get-execution-results-by-block?${params}`, {
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
| `blockId` | string | yes | Block ID for the execution result lookup. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_links": {},
      "block_id": "string",
      "chunks": [
        {}
      ],
      "events": [
        {}
      ],
      "id": "string",
      "previous_result_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_links` | object | Flow API resource links. |
| `block_id` | string | Block ID for the execution result. |
| `chunks` | array<object> | Execution chunks. |
| `events` | array<object> | Events included in the execution result. |
| `id` | string | Flow execution result ID. |
| `previous_result_id` | string | Previous execution result ID. |

## Native endpoint

Through the native Flow Blockchain API, this operation is `GET /execution_results` (base URL `https://rest-mainnet.onflow.org/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-execution-results-by-block.md) for the provider-specific parameters and requirements.

