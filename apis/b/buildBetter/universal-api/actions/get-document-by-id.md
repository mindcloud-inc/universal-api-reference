# BuildBetter: Get Document By ID



```
GET https://connect.mindcloud.co/v1/universal/buildBetter/latest/actions/get-document-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BuildBetter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/buildBetter/latest/actions/get-document-by-id?connectionId=$CONNECTION_ID&id=12345" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "12345"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/buildBetter/latest/actions/get-document-by-id?${params}`, {
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
| `id` | string | yes | BuildBetter document ID. Example: `12345`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "permission": "string",
      "source": "string",
      "status": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "user_instructions": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string | Rendered document content. |
| `created_at` | date | Created timestamp. |
| `id` | string | BuildBetter document identifier. |
| `name` | string | Document name. |
| `permission` | string | Document permission mode. |
| `source` | string | Document source classification. |
| `status` | string | Document status. |
| `updated_at` | date | Last updated timestamp. |
| `user_instructions` | string | User-supplied instructions. |

## Native endpoint

Through the native BuildBetter API, this operation is `POST /graphql` (base URL `https://api.buildbetter.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document-by-id.md) for the provider-specific parameters and requirements.

