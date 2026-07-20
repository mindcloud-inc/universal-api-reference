# Crossmint: Create Collection

Creates a collection in Crossmint.

```
POST https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/create-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crossmint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/create-collection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "chain": "base-sepolia",
  "metadata.name": "MindCloud Test Collection",
  "metadata.description": "Collection created by MindCloud for Crossmint runtime testing.",
  "metadata.imageUrl": "https://www.crossmint.com/assets/crossmint/logo.png",
  "metadata.symbol": "MCTEST",
  "fungibility": "non-fungible"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/create-collection', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "chain": "base-sepolia",
    "metadata.name": "MindCloud Test Collection",
    "metadata.description": "Collection created by MindCloud for Crossmint runtime testing.",
    "metadata.imageUrl": "https://www.crossmint.com/assets/crossmint/logo.png",
    "metadata.symbol": "MCTEST",
    "fungibility": "non-fungible"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `chain` | string | yes | Blockchain for the collection. Default: `base-sepolia`. |
| `metadata.name` | string | yes | Collection display name. Example: `MindCloud Test Collection`. |
| `metadata.description` | string | yes | Collection description. Example: `Collection created by MindCloud for Crossmint runtime testing.`. |
| `metadata.imageUrl` | string | yes | Collection image URL. Default: `https://www.crossmint.com/assets/crossmint/logo.png`. |
| `metadata.symbol` | string | yes | Collection symbol. Default: `MCTEST`. |
| `fungibility` | string | yes | Collection fungibility. Default: `non-fungible`. |
| `transferable` | boolean | no | Whether NFTs are transferable. Default: `true`. |
| `supplyLimit` | number | no | Maximum supply for the collection. Default: `10`. |
| `payments.price` | string | no | Mint price for the collection. Default: `0.0001`. |
| `payments.recipientAddress` | string | no | Address that receives collection payments. Example: `0x1234567890123456789012345678901234567890`. |
| `payments.currency` | string | no | Currency for collection payments. Default: `eth`. |
| `reuploadLinkedFiles` | boolean | no | Whether metadata URLs are reuploaded to IPFS. Default: `true`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Crossmint API returns.

## Native endpoint

Through the native Crossmint API, this operation is `POST /2022-06-09/collections` (base URL `https://staging.crossmint.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-collection.md) for the provider-specific parameters and requirements.

