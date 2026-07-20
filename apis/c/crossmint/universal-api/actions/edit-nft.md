# Crossmint: Edit NFT

Updates NFT metadata in Crossmint.

```
PUT https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/edit-nft
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crossmint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/edit-nft" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "collectionId": "2b93e85e-d500-4f14-8a76-515c604e59ff",
  "id": "b398a6e7-4b6d-4097-869c-33dd1f454629",
  "metadata": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/edit-nft', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "collectionId": "2b93e85e-d500-4f14-8a76-515c604e59ff",
    "id": "b398a6e7-4b6d-4097-869c-33dd1f454629",
    "metadata": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `collectionId` | string | yes | Collection identifier. Default: `2b93e85e-d500-4f14-8a76-515c604e59ff`. Example: `2b93e85e-d500-4f14-8a76-515c604e59ff`. |
| `id` | string | yes | NFT identifier returned by Crossmint. Default: `b398a6e7-4b6d-4097-869c-33dd1f454629`. Example: `b398a6e7-4b6d-4097-869c-33dd1f454629`. |
| `metadata` | object | yes | Updated NFT metadata object. Example: `[object Object]`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `reuploadLinkedFiles` | boolean | no | Whether metadata URLs should be resolved and reuploaded to IPFS. Defaults to true. Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "action": "string",
      "actionId": "string",
      "data": {},
      "resource": "string",
      "startedAt": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action` | string | Crossmint action type. |
| `actionId` | string | NFT update action identifier. |
| `data` | object | NFT update payload details. |
| `resource` | string | Action resource URL. |
| `startedAt` | string | When the update started. |
| `status` | string | Current processing status. |

## Native endpoint

Through the native Crossmint API, this operation is `PATCH /2022-06-09/collections/:collectionId/nfts/:id` (base URL `https://staging.crossmint.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/edit-nft.md) for the provider-specific parameters and requirements.

