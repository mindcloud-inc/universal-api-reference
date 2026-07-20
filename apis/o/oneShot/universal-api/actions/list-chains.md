# 1Shot: List Chains

Retrieves supported blockchain networks from 1Shot API.

```
GET https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/list-chains
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 1Shot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/list-chains?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/list-chains?${params}`, {
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
      "averageBlockMiningTime": 1,
      "chainId": 1,
      "name": "Ava Chen",
      "nativeCurrency": {
        "decimals": 1,
        "name": "Ava Chen",
        "symbol": "string"
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `averageBlockMiningTime` | number |  |
| `chainId` | number |  |
| `name` | string |  |
| `nativeCurrency.decimals` | number |  |
| `nativeCurrency.name` | string |  |
| `nativeCurrency.symbol` | string |  |
| `type` | string |  |

## Native endpoint

Through the native 1Shot API, this operation is `GET /chains` (base URL `https://api.1shotapi.com/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-chains.md) for the provider-specific parameters and requirements.

