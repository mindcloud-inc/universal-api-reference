# Mempool: Get Mempool Summary

Retrieves current mempool backlog statistics from Mempool.

```
GET https://connect.mindcloud.co/v1/universal/mempool/latest/actions/get-mempool-summary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mempool `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mempool/latest/actions/get-mempool-summary?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mempool/latest/actions/get-mempool-summary?${params}`, {
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
      "count": 1,
      "fee_histogram": [
        [
          "string"
        ]
      ],
      "total_fee": 1,
      "vsize": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `fee_histogram` | array<array> |  |
| `total_fee` | number |  |
| `vsize` | number |  |

## Native endpoint

Through the native Mempool API, this operation is `GET /mempool` (base URL `https://mempool.space/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-mempool-summary.md) for the provider-specific parameters and requirements.

