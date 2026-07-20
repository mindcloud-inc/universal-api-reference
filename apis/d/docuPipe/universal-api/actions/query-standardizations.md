# DocuPipe: Query Standardizations

Queries standardizations in DocuPipe.

```
POST https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/query-standardizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPipe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/query-standardizations" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "schemaId": "string",
  "query": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/query-standardizations', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "schemaId": "string",
    "query": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `schemaId` | string | yes | Unique identifier of the schema. |
| `query` | string | yes | Free language text explaining what documents you're after. if the text is empty |
| `dataset` | string | no | Name of the dataset to which the document belongs If empty, the query will run on all documents |
| `limit` | number | no | Maximum number of documents to return. If not specified will default to 100 Default: `100`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "queryFeedback": "string",
      "standardizations": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `queryFeedback` | string | AI generated feedback on the query, which may include suggestions for improvement, ambiguities, or explanation about the query feasibility |
| `standardizations` | array<object> | List of document standardization objects that match the query. |

## Native endpoint

Through the native DocuPipe API, this operation is `POST /query` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-standardizations.md) for the provider-specific parameters and requirements.

