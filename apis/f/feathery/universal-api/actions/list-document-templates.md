# Feathery: List Document Templates



```
GET https://connect.mindcloud.co/v1/universal/feathery/latest/actions/list-document-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Feathery `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/feathery/latest/actions/list-document-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/feathery/latest/actions/list-document-templates?${params}`, {
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
| `name` | string | no | Only return document templates whose names contain this value. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tags` | string | no | Tag filter values. Feathery treats repeated `tags` query parameters as AND conditions and `;;` within one value as OR. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "file": "string",
      "id": "string",
      "name": "Ava Chen",
      "tags": [
        "string"
      ],
      "type": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date | When the document was created. |
| `file` | string | Document file URL. |
| `id` | string | Document ID. |
| `name` | string | Document name. |
| `tags` | array<string> | Document tags. |
| `type` | string | Document type. |
| `updated_at` | date | When the document was last updated. |

## Native endpoint

Through the native Feathery API, this operation is `GET /api/document/template/` (base URL `https://api.feathery.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-document-templates.md) for the provider-specific parameters and requirements.

