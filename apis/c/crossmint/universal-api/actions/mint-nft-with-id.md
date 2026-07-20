# Crossmint: Mint NFT with ID

Mints an NFT with an ID in Crossmint.

```
POST https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/mint-nft-with-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crossmint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/mint-nft-with-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "collectionId": "2b93e85e-d500-4f14-8a76-515c604e59ff",
  "id": "stage3-nft-001",
  "metadata": "[object Object]",
  "recipient": "email:apps@mindcloud.co:polygon"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/mint-nft-with-id', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "collectionId": "2b93e85e-d500-4f14-8a76-515c604e59ff",
    "id": "stage3-nft-001",
    "metadata": "[object Object]",
    "recipient": "email:apps@mindcloud.co:polygon"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `collectionId` | string | yes | Collection identifier. Use a real Crossmint collection or credential-template-backed collection ID. Default: `2b93e85e-d500-4f14-8a76-515c604e59ff`. Example: `2b93e85e-d500-4f14-8a76-515c604e59ff`. |
| `id` | string | yes | Custom NFT identifier used as the idempotency key. Example: `stage3-nft-001`. |
| `metadata` | object | yes | NFT metadata object. Provide at least `name`, `image`, and `description`. Example: `[object Object]`. |
| `recipient` | string | yes | Recipient in `<chain>:<address>` or `email:<email_address>:<chain>` format. Example: `email:apps@mindcloud.co:polygon`. |
| `sendNotification` | boolean | no | Notify the recipient by email after minting. Defaults to true. Default: `true`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `locale` | string | no | Locale for notification content. Defaults to `en-US`. Default: `en-US`. Example: `en-US`. |
| `reuploadLinkedFiles` | boolean | no | Whether metadata URLs should be resolved and reuploaded to IPFS. Defaults to true. Default: `true`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Crossmint API returns.

## Native endpoint

Through the native Crossmint API, this operation is `PUT /2022-06-09/collections/:collectionId/nfts/:id` (base URL `https://staging.crossmint.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/mint-nft-with-id.md) for the provider-specific parameters and requirements.

