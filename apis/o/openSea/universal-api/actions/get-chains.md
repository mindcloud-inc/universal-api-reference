# OpenSea: Get Supported Chains Catalog

Retrieves supported chains from OpenSea.

```
GET https://connect.mindcloud.co/v1/universal/openSea/latest/actions/get-chains
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenSea `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openSea/latest/actions/get-chains?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openSea/latest/actions/get-chains?${params}`, {
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
      "result": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | object |  |

## Native endpoint

Through the native OpenSea API, this operation is `GET /api/v2/chains` (base URL `https://api.opensea.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-chains.md) for the provider-specific parameters and requirements.

