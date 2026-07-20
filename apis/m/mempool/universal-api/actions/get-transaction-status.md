# Mempool: Get Transaction Status

Retrieves transaction confirmation status from Mempool.

```
GET https://connect.mindcloud.co/v1/universal/mempool/latest/actions/get-transaction-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mempool `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mempool/latest/actions/get-transaction-status?connectionId=$CONNECTION_ID&txid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "txid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mempool/latest/actions/get-transaction-status?${params}`, {
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
| `txid` | string | yes | Bitcoin transaction ID to inspect. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "block_hash": "string",
      "block_height": 1,
      "block_time": 1,
      "confirmed": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `block_hash` | string |  |
| `block_height` | number |  |
| `block_time` | number |  |
| `confirmed` | boolean |  |

## Native endpoint

Through the native Mempool API, this operation is `GET /tx/[:txid]/status` (base URL `https://mempool.space/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transaction-status.md) for the provider-specific parameters and requirements.

