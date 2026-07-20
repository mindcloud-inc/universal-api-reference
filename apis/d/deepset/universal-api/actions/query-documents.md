# Deepset: Query Documents

Queries documents in a Deepset index.

```
GET https://connect.mindcloud.co/v1/universal/deepset/latest/actions/query-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deepset `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepset/latest/actions/query-documents?connectionId=$CONNECTION_ID&indexName=Ava%20Chen&query=string&workspaceName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "indexName": "Ava Chen",
  "query": "string",
  "workspaceName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepset/latest/actions/query-documents?${params}`, {
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
| `indexName` | string | yes | deepset index name. |
| `query` | string | yes | Document query payload. |
| `workspaceName` | string | yes | deepset workspace name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "id": "string",
      "score": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string |  |
| `id` | string |  |
| `score` | number |  |

## Native endpoint

Through the native Deepset API, this operation is `POST /api/v1/workspaces/:workspace_name/indexes/:index_name/documents-query` (base URL `https://api.cloud.deepset.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-documents.md) for the provider-specific parameters and requirements.

