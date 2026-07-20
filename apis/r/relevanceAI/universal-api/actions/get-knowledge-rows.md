# Relevance AI: Retrieve Knowledge Set Rows



```
GET https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/get-knowledge-rows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Relevance AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/get-knowledge-rows?connectionId=$CONNECTION_ID&knowledgeSet=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "knowledgeSet": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/get-knowledge-rows?${params}`, {
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
| `knowledgeSet` | string | yes | The knowledge set id to read rows from. |
| `pageSize` | number | no | Maximum number of rows to return. Default: `5`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "alias": "string",
      "data": {
        "email": "ava@example.com"
      },
      "document_id": "string",
      "insert_date_": "2026-05-07T12:00:00.000Z",
      "is_chunked": true,
      "is_vectorized": true,
      "knowledge_set": "string",
      "update_date_": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string | The knowledge row ID. |
| `alias` | string | The row alias. |
| `data.email` | string | The email value stored in the row. |
| `document_id` | string | The document ID. |
| `insert_date_` | date | When the row was inserted. |
| `is_chunked` | boolean | Whether the row has been chunked. |
| `is_vectorized` | boolean | Whether the row has been vectorized. |
| `knowledge_set` | string | The knowledge set name. |
| `update_date_` | date | When the row was last updated. |

## Native endpoint

Through the native Relevance AI API, this operation is `POST /knowledge/list` (base URL `https://api-{{credentials.region}}.stack.tryrelevance.com/latest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-knowledge-rows.md) for the provider-specific parameters and requirements.

