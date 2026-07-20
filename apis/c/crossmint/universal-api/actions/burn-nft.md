# Crossmint: Burn NFT

Burns an NFT from Crossmint.

```
DELETE https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/burn-nft
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crossmint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/burn-nft?connectionId=$CONNECTION_ID&collectionId=2b93e85e-d500-4f14-8a76-515c604e59ff&id=b398a6e7-4b6d-4097-869c-33dd1f454629" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "collectionId": "2b93e85e-d500-4f14-8a76-515c604e59ff",
  "id": "b398a6e7-4b6d-4097-869c-33dd1f454629"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/burn-nft?${params}`, {
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
| `id` | string | yes | NFT identifier returned by Crossmint. Default: `b398a6e7-4b6d-4097-869c-33dd1f454629`. Example: `b398a6e7-4b6d-4097-869c-33dd1f454629`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "action": "string",
      "actionId": "string",
      "completedAt": "string",
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
| `actionId` | string | NFT burn action identifier. |
| `completedAt` | string | When the burn completed, when available. |
| `data` | object | NFT burn payload details. |
| `resource` | string | Action resource URL. |
| `startedAt` | string | When the burn started. |
| `status` | string | Current processing status. |

## Native endpoint

Through the native Crossmint API, this operation is `DELETE /2022-06-09/collections/:collectionId/nfts/:id` (base URL `https://staging.crossmint.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/burn-nft.md) for the provider-specific parameters and requirements.

