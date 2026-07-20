# Mempool: Get Block Transaction ID at Index

Retrieves a block transaction ID from Mempool by index.

```
GET https://connect.mindcloud.co/v1/universal/mempool/latest/actions/get-block-transaction-id-at-index
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mempool `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mempool/latest/actions/get-block-transaction-id-at-index?connectionId=$CONNECTION_ID&hash=string&index=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "hash": "string",
  "index": "0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mempool/latest/actions/get-block-transaction-id-at-index?${params}`, {
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
| `hash` | string | yes | Block hash to inspect. |
| `index` | number | yes | Zero-based transaction index within the block. Default: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<number> | Raw response bytes. |
| `type` | string | Node buffer response marker. |

## Native endpoint

Through the native Mempool API, this operation is `GET /block/[:hash]/txid/[:index]` (base URL `https://mempool.space/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-block-transaction-id-at-index.md) for the provider-specific parameters and requirements.

