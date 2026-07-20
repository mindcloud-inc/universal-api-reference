# Mempool: Get Tip Hash

Retrieves the current block hash from Mempool.

```
GET https://connect.mindcloud.co/v1/universal/mempool/latest/actions/get-tip-hash
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mempool `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mempool/latest/actions/get-tip-hash?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mempool/latest/actions/get-tip-hash?${params}`, {
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

Through the native Mempool API, this operation is `GET /blocks/tip/hash` (base URL `https://mempool.space/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tip-hash.md) for the provider-specific parameters and requirements.

