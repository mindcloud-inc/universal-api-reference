# OpenSea: Get NFT Metadata

Retrieves NFT metadata from OpenSea.

```
GET https://connect.mindcloud.co/v1/universal/openSea/latest/actions/get-nft-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenSea `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openSea/latest/actions/get-nft-metadata?connectionId=$CONNECTION_ID&chain=string&contractAddress=string&tokenId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chain": "string",
  "contractAddress": "string",
  "tokenId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openSea/latest/actions/get-nft-metadata?${params}`, {
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
| `chain` | string | yes | The blockchain on which to filter the results |
| `contractAddress` | string | yes | The unique public blockchain identifier for the contract |
| `tokenId` | string | yes | The NFT token id |

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

Through the native OpenSea API, this operation is `GET /api/v2/metadata/{chain}/{contractAddress}/{tokenId}` (base URL `https://api.opensea.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-nft-metadata.md) for the provider-specific parameters and requirements.

