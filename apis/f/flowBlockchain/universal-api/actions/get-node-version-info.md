# Flow Blockchain: Get Node Version Info

Retrieves node version information from Flow Blockchain.

```
GET https://connect.mindcloud.co/v1/universal/flowBlockchain/latest/actions/get-node-version-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flow Blockchain `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flowBlockchain/latest/actions/get-node-version-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flowBlockchain/latest/actions/get-node-version-info?${params}`, {
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
      "commit": "string",
      "compatible_range": {},
      "node_root_block_height": "string",
      "protocol_state_version": "string",
      "protocol_version": "string",
      "semver": "string",
      "spork_id": "string",
      "spork_root_block_height": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `commit` | string | Node build commit. |
| `compatible_range` | object | Compatible block-height range. |
| `node_root_block_height` | string | Node root block height. |
| `protocol_state_version` | string | Protocol state version. |
| `protocol_version` | string | Flow protocol version. |
| `semver` | string | Node semantic version. |
| `spork_id` | string | Current spork ID. |
| `spork_root_block_height` | string | Spork root block height. |

## Native endpoint

Through the native Flow Blockchain API, this operation is `GET /node_version_info` (base URL `https://rest-mainnet.onflow.org/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-node-version-info.md) for the provider-specific parameters and requirements.

