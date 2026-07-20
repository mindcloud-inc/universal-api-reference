# Cody: List Documents



```
GET https://connect.mindcloud.co/v1/universal/cody/latest/actions/list-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cody `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cody/latest/actions/list-documents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cody/latest/actions/list-documents?${params}`, {
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
| `folderId` | string | no | Id of the folder to list documents for. |
| `conversationId` | string | no | Id of the conversation to only list documents the conversation is focused on. |
| `keyword` | string | no | Keyword to filter the list to documents that partially match the name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentUrl": "https://example.com",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "folderId": "string",
      "id": "string",
      "name": "Ava Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentUrl` | string | Document content URL. |
| `createdAt` | date | Document creation timestamp. |
| `folderId` | string | Parent folder identifier. |
| `id` | string | Document identifier. |
| `name` | string | Document name. |
| `status` | string | Document sync status. |

## Native endpoint

Through the native Cody API, this operation is `GET /documents` (base URL `https://getcody.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-documents.md) for the provider-specific parameters and requirements.

