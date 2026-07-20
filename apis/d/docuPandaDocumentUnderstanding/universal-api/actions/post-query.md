# DocuPanda - Document Understanding: Query Standardizations

Creates a natural-language standardization query in DocuPanda.

```
POST https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/post-query
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPanda - Document Understanding `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/post-query" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "query": "string",
  "schemaId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/post-query', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "query": "string",
    "schemaId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dataset` | string | no | Name of the dataset to which the document belongs If empty, the query will run on all documents |
| `limit` | number | no | Maximum number of documents to return. If not specified will default to 100 |
| `query` | string | yes | Free language text explaining what documents you're after. if the text is empty |
| `schemaId` | string | yes | Unique identifier of the schema. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "queryFeedback": "string",
      "standardizations": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `queryFeedback` | string |  |
| `standardizations` | array<string> | List of document standardization objects that match the query. |

## Native endpoint

Through the native DocuPanda - Document Understanding API, this operation is `POST /query` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-query.md) for the provider-specific parameters and requirements.

