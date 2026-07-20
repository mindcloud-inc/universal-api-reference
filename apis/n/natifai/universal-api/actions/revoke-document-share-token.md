# Natif.ai: Revoke Document Share Token

Deletes an existing document sharing token from Natif.ai.

```
DELETE https://connect.mindcloud.co/v1/universal/natifai/latest/actions/revoke-document-share-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Natif.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/natifai/latest/actions/revoke-document-share-token?connectionId=$CONNECTION_ID&tokenUuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tokenUuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/natifai/latest/actions/revoke-document-share-token?${params}`, {
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
| `tokenUuid` | string | yes | UUID of the sharing token to revoke. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Natif.ai API returns.

## Native endpoint

Through the native Natif.ai API, this operation is `DELETE /share-tokens/documents` (base URL `https://api.natif.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/revoke-document-share-token.md) for the provider-specific parameters and requirements.

