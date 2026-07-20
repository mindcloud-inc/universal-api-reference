# DocuPanda - Document Understanding: AutoGenerate a Schema

Creates a schema from documents in DocuPanda.

```
POST https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/post-schema-autogenerate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPanda - Document Understanding `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/post-schema-autogenerate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "schemaName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/post-schema-autogenerate', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "schemaName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentIds` | list<string> | no | List of document IDs to use for schema generation. |
| `queries` | list<string> | no | List of example questions you would want to ask of your documents. |
| `schemaName` | string | yes | Name of the schema to be defined. For example rental contracts |
| `documentIds[]` | array<string> | no | List of document IDs to use for schema generation. |
| `dataset` | string | no | The dataset to which the documents belong. |
| `instructions` | string | no | Instructions on how to create the schema. |
| `guidelines` | string | no | Guidelines to apply to the schema to documents when standardizing. |
| `standardizeUsingSchema` | boolean | no | Whether to standardize the input documents using the newly created schema after generation.Note that standardizing documents costs credits just as if you had called the `/standardize` endpoint directly |
| `standardizationMode` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "jobId": "string",
      "schemaId": "string",
      "schemaName": "Ava Chen",
      "status": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `jobId` | string | Unique identifier for the autogenerate schema job. |
| `schemaId` | string | Unique identifier for the schema being generated. The schema is only available when the job is completed. |
| `schemaName` | string | Name of the schema being generated. |
| `status` | object |  |

## Native endpoint

Through the native DocuPanda - Document Understanding API, this operation is `POST /schema/autogenerate` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-schema-autogenerate.md) for the provider-specific parameters and requirements.

