# Crossmint: Create Collection Idempotent

Creates a collection idempotently in Crossmint.

```
POST https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/create-collection-idempotent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crossmint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/create-collection-idempotent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "collectionId": "mindcloud-crossmint-test-collection",
  "chain": "base-sepolia",
  "metadata.name": "MindCloud Test Collection",
  "metadata.description": "Collection created by MindCloud for Crossmint runtime testing.",
  "metadata.imageUrl": "https://www.crossmint.com/assets/crossmint/logo.png",
  "metadata.symbol": "MCTEST2"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/create-collection-idempotent', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "collectionId": "mindcloud-crossmint-test-collection",
    "chain": "base-sepolia",
    "metadata.name": "MindCloud Test Collection",
    "metadata.description": "Collection created by MindCloud for Crossmint runtime testing.",
    "metadata.imageUrl": "https://www.crossmint.com/assets/crossmint/logo.png",
    "metadata.symbol": "MCTEST2"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `collectionId` | string | yes | Custom collection identifier. Example: `mindcloud-crossmint-test-collection`. |
| `chain` | string | yes | Blockchain for the collection. Default: `base-sepolia`. |
| `metadata.name` | string | yes | Collection display name. Example: `MindCloud Test Collection`. |
| `metadata.description` | string | yes | Collection description. Example: `Collection created by MindCloud for Crossmint runtime testing.`. |
| `metadata.imageUrl` | string | yes | Collection image URL. Default: `https://www.crossmint.com/assets/crossmint/logo.png`. |
| `metadata.symbol` | string | yes | Collection symbol. Default: `MCTEST2`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Crossmint API returns.

## Native endpoint

Through the native Crossmint API, this operation is `PUT /2022-06-09/collections/:collectionId` (base URL `https://staging.crossmint.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-collection-idempotent.md) for the provider-specific parameters and requirements.

