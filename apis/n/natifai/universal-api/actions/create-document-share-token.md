# Natif.ai: Create Document Share Token

Creates a document sharing token in Natif.ai.

```
POST https://connect.mindcloud.co/v1/universal/natifai/latest/actions/create-document-share-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Natif.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/natifai/latest/actions/create-document-share-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentId": "string",
  "expiresAt": "2026-04-14"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/natifai/latest/actions/create-document-share-token', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentId": "string",
    "expiresAt": "2026-04-14"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentId` | string | yes | UUID of the document to share. |
| `expiresAt` | string | yes | Expiration date for the share token in YYYY-MM-DD format. Tokens expire at 00:00:00 UTC on this date. Example: `2026-04-14`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "document_id": "string",
      "expires_at": "2026-05-07T12:00:00.000Z",
      "issuer_user_id": "string",
      "last_used_at": "2026-05-07T12:00:00.000Z",
      "tenant_id": "string",
      "token": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `document_id` | string |  |
| `expires_at` | date |  |
| `issuer_user_id` | string |  |
| `last_used_at` | date |  |
| `tenant_id` | string |  |
| `token` | string | Share token value returned by Natif. |
| `uuid` | string | Sharing token ID. |

## Native endpoint

Through the native Natif.ai API, this operation is `POST /share-tokens/documents` (base URL `https://api.natif.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-document-share-token.md) for the provider-specific parameters and requirements.

