# Readwise: Bulk Update Reader Documents

Updates multiple documents in Readwise Reader.

```
PUT https://connect.mindcloud.co/v1/universal/readwise/latest/actions/bulk-update-reader-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Readwise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/readwise/latest/actions/bulk-update-reader-documents" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "updates": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/readwise/latest/actions/bulk-update-reader-documents', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "updates": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `updates` | list<object> | yes | List of update objects. Each item must include id and may include title, author, summary, published_date, image_url, seen, location, category, tags, or notes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": "string",
      "id": "string",
      "results": [
        {}
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | string |  |
| `id` | string |  |
| `results[]` | object |  |
| `success` | boolean |  |

## Native endpoint

Through the native Readwise API, this operation is `PATCH /api/v3/bulk_update/` (base URL `https://readwise.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-update-reader-documents.md) for the provider-specific parameters and requirements.

