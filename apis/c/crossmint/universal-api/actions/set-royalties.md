# Crossmint: Set Royalties

Updates collection royalties in Crossmint.

```
PUT https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/set-royalties
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crossmint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/set-royalties" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "collectionId": "string",
  "recipients[0].address": "0x1234567890123456789012345678901234567890",
  "recipients[0].basisPoints": "100"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/set-royalties', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "collectionId": "string",
    "recipients[0].address": "0x1234567890123456789012345678901234567890",
    "recipients[0].basisPoints": "100"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `collectionId` | string | yes | Collection identifier. |
| `recipients[0].address` | string | yes | Royalty recipient address. Example: `0x1234567890123456789012345678901234567890`. |
| `recipients[0].basisPoints` | number | yes | Royalty share in basis points. Default: `100`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Crossmint API returns.

## Native endpoint

Through the native Crossmint API, this operation is `PUT /v1-alpha1/minting/collections/:collectionId/royalties` (base URL `https://staging.crossmint.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-royalties.md) for the provider-specific parameters and requirements.

