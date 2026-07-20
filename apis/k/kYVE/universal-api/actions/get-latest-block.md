# KYVE: Get Latest Block



```
GET https://connect.mindcloud.co/v1/universal/kYVE/latest/actions/get-latest-block
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KYVE `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kYVE/latest/actions/get-latest-block?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kYVE/latest/actions/get-latest-block?${params}`, {
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
      "block": {},
      "block_id": {},
      "sdk_block": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `block` | object |  |
| `block_id` | object |  |
| `sdk_block` | object |  |

## Native endpoint

Through the native KYVE API, this operation is `GET /cosmos/base/tendermint/v1beta1/blocks/latest` (base URL `https://api.kyve.network`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-latest-block.md) for the provider-specific parameters and requirements.

