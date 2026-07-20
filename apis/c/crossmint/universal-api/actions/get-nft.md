# Crossmint: Get NFT

Retrieves NFT status from Crossmint.

```
GET https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/get-nft
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crossmint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/get-nft?connectionId=$CONNECTION_ID&collectionId=2b93e85e-d500-4f14-8a76-515c604e59ff&id=1394c116-a808-4a5c-8cf5-4102c765f332" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "collectionId": "2b93e85e-d500-4f14-8a76-515c604e59ff",
  "id": "1394c116-a808-4a5c-8cf5-4102c765f332"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/get-nft?${params}`, {
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
| `collectionId` | string | yes | Collection identifier. Default: `2b93e85e-d500-4f14-8a76-515c604e59ff`. Example: `2b93e85e-d500-4f14-8a76-515c604e59ff`. |
| `id` | string | yes | NFT identifier returned by Crossmint. Default: `1394c116-a808-4a5c-8cf5-4102c765f332`. Example: `1394c116-a808-4a5c-8cf5-4102c765f332`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "action": "string",
      "id": "string",
      "onChain": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action` | string | Action status URL returned by Crossmint. |
| `id` | string | NFT identifier returned by Crossmint. |
| `onChain` | object | On-chain NFT status details. |

## Native endpoint

Through the native Crossmint API, this operation is `GET /2022-06-09/collections/:collectionId/nfts/:id` (base URL `https://staging.crossmint.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-nft.md) for the provider-specific parameters and requirements.

