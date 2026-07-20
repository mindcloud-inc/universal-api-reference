# Underdog Protocol: Get Legacy NFT

Retrieves a legacy NFT from Underdog Protocol.

```
GET https://connect.mindcloud.co/v1/universal/underdogProtocol/latest/actions/get-legacy-nft
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Underdog Protocol `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/underdogProtocol/latest/actions/get-legacy-nft?connectionId=$CONNECTION_ID&mintAddress=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mintAddress": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/underdogProtocol/latest/actions/get-legacy-nft?${params}`, {
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
| `mintAddress` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Underdog Protocol API returns.

## Native endpoint

Through the native Underdog Protocol API, this operation is `GET /v1/nfts/:mintAddress` (base URL `https://dev.underdogprotocol.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-legacy-nft.md) for the provider-specific parameters and requirements.

