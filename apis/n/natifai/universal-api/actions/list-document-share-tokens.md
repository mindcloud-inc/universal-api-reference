# Natif.ai: List Document Share Tokens

Retrieves document sharing tokens from Natif.ai.

```
GET https://connect.mindcloud.co/v1/universal/natifai/latest/actions/list-document-share-tokens
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Natif.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/natifai/latest/actions/list-document-share-tokens?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/natifai/latest/actions/list-document-share-tokens?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native Natif.ai API, this operation is `GET /share-tokens/documents` (base URL `https://api.natif.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-document-share-tokens.md) for the provider-specific parameters and requirements.

