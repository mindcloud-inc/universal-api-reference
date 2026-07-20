# Crossmint: Mint NFT

Mints an NFT in Crossmint.

```
POST https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/mint-nft
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crossmint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/mint-nft" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "collectionId": "string",
  "metadata.name": "MindCloud Test NFT",
  "metadata.image": "https://www.crossmint.com/assets/crossmint/logo.png",
  "metadata.description": "NFT minted by MindCloud for Crossmint runtime testing.",
  "recipient": "email:user@example.com:base-sepolia"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/mint-nft', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "collectionId": "string",
    "metadata.name": "MindCloud Test NFT",
    "metadata.image": "https://www.crossmint.com/assets/crossmint/logo.png",
    "metadata.description": "NFT minted by MindCloud for Crossmint runtime testing.",
    "recipient": "email:user@example.com:base-sepolia"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `collectionId` | string | yes | Collection identifier. |
| `metadata.name` | string | yes | NFT name. Example: `MindCloud Test NFT`. |
| `metadata.image` | string | yes | NFT image URL. Default: `https://www.crossmint.com/assets/crossmint/logo.png`. |
| `metadata.description` | string | yes | NFT description. Example: `NFT minted by MindCloud for Crossmint runtime testing.`. |
| `recipient` | string | yes | Recipient locator for the minted NFT. Example: `email:user@example.com:base-sepolia`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Crossmint API returns.

## Native endpoint

Through the native Crossmint API, this operation is `POST /2022-06-09/collections/:collectionId/nfts` (base URL `https://staging.crossmint.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/mint-nft.md) for the provider-specific parameters and requirements.

