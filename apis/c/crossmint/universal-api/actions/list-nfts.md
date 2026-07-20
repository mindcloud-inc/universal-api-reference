# Crossmint: List NFTs

Retrieves NFTs from a Crossmint collection.

```
GET https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/list-nfts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crossmint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/list-nfts?connectionId=$CONNECTION_ID&collectionId=2b93e85e-d500-4f14-8a76-515c604e59ff&page=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "collectionId": "2b93e85e-d500-4f14-8a76-515c604e59ff",
  "page": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/list-nfts?${params}`, {
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
| `collectionId` | string | yes | Collection identifier. For credential-template-backed tests, use the template ID returned by Crossmint. Default: `2b93e85e-d500-4f14-8a76-515c604e59ff`. Example: `2b93e85e-d500-4f14-8a76-515c604e59ff`. |
| `page` | number | yes | Page number starting at 1. Default: `1`. |
| `perPage` | number | no | How many items to return in the page. Default: `20`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "metadata": {},
      "onChain": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | NFT identifier returned by Crossmint. |
| `metadata` | object | NFT metadata object when available. |
| `onChain` | object | On-chain NFT status details. |

## Native endpoint

Through the native Crossmint API, this operation is `GET /2022-06-09/collections/:collectionId/nfts` (base URL `https://staging.crossmint.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-nfts.md) for the provider-specific parameters and requirements.

