# Cataas: List Cats



```
GET https://connect.mindcloud.co/v1/universal/cataas/latest/actions/list-cats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cataas `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cataas/latest/actions/list-cats?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cataas/latest/actions/list-cats?${params}`, {
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
| `tags` | string | no | Return only cats matching this tag expression. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "id": "string",
      "mimetype": "string",
      "tags": [
        "string"
      ],
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string | Timestamp returned by the current Cataas runtime. |
| `id` | string | Cat identifier. |
| `mimetype` | string | Media MIME type. |
| `tags` | array<string> | Tags associated with the cat. |
| `url` | string | Direct Cataas URL returned by the current runtime. |

## Native endpoint

Through the native Cataas API, this operation is `GET /api/cats` (base URL `https://cataas.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-cats.md) for the provider-specific parameters and requirements.

