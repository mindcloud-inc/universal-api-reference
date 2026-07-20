# Docutray: List Document Types



```
GET https://connect.mindcloud.co/v1/universal/docutray/latest/actions/list-document-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docutray `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docutray/latest/actions/list-document-types?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docutray/latest/actions/list-document-types?${params}`, {
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
| `search` | string | no | Search by name, code, or description of the document type |

## Response

```json
{
  "success": true,
  "data": [
    {
      "codeType": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "isDraft": true,
      "isPublic": true,
      "name": "Ava Chen",
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `codeType` | string |  |
| `createdAt` | date |  |
| `description` | string |  |
| `id` | string |  |
| `isDraft` | boolean |  |
| `isPublic` | boolean |  |
| `name` | string |  |
| `status` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Docutray API, this operation is `GET api/document-types` (base URL `https://app.docutray.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-document-types.md) for the provider-specific parameters and requirements.

