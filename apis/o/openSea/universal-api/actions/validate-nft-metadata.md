# OpenSea: Validate NFT Metadata

Validates NFT metadata in OpenSea.

```
PUT https://connect.mindcloud.co/v1/universal/openSea/latest/actions/validate-nft-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenSea `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/openSea/latest/actions/validate-nft-metadata" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "chain": "string",
  "address": "string",
  "identifier": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/openSea/latest/actions/validate-nft-metadata', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "chain": "string",
    "address": "string",
    "identifier": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `chain` | string | yes | The blockchain on which to filter the results |
| `address` | string | yes | The contract address |
| `identifier` | string | yes | The NFT token id |
| `ignoreCachedItemUrls` | boolean | no | Whether to bypass cached SeaDN URLs |

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

Through the native OpenSea API, this operation is `POST /api/v2/chain/{chain}/contract/{address}/nfts/{identifier}/validate-metadata` (base URL `https://api.opensea.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-nft-metadata.md) for the provider-specific parameters and requirements.

