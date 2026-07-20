# Etherscan: Get Block Number by Timestamp

Retrieves a block number by timestamp.

```
GET https://connect.mindcloud.co/v1/universal/etherscan/latest/actions/get-block-number-by-timestamp
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Etherscan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/etherscan/latest/actions/get-block-number-by-timestamp?connectionId=$CONNECTION_ID&timestamp=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "timestamp": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/etherscan/latest/actions/get-block-number-by-timestamp?${params}`, {
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
| `chainId` | string | no | Default: `1`. |
| `timestamp` | number | yes |  |
| `closest` | string | no | Default: `before`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "result": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Etherscan response message. |
| `result` | string | Block number returned for the timestamp. |
| `status` | string | Etherscan status code. |

## Native endpoint

Through the native Etherscan API, this operation is `GET /v2/api` (base URL `https://api.etherscan.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-block-number-by-timestamp.md) for the provider-specific parameters and requirements.

