# Flow Blockchain: Get Blocks by ID

Retrieves blocks from Flow Blockchain by ID.

```
GET https://connect.mindcloud.co/v1/universal/flowBlockchain/latest/actions/get-blocks-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flow Blockchain `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flowBlockchain/latest/actions/get-blocks-by-id?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flowBlockchain/latest/actions/get-blocks-by-id?${params}`, {
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
| `id` | string | yes | Block ID to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_expandable": {},
      "_links": {},
      "block_status": "string",
      "header": {}
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
| `block_status` | string | Flow block status. |
| `header` | object | Block header metadata. |

## Native endpoint

Through the native Flow Blockchain API, this operation is `GET /blocks/{id}` (base URL `https://rest-mainnet.onflow.org/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-blocks-by-id.md) for the provider-specific parameters and requirements.

