# DocuPipe: AutoGenerate a Schema

Generates a schema in DocuPipe.

```
POST https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/auto-generate-a-schema
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPipe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/auto-generate-a-schema" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/auto-generate-a-schema', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `schemaName` | string | no | Name of the schema to be defined. For example rental contracts |
| `documentIds[]` | array<string> | no | List of document IDs to use for schema generation. |
| `dataset` | string | no | The dataset to which the documents belong. |
| `instructions` | string | no | Instructions on how to create the schema. |
| `guidelines` | string | no | Guidelines to apply to the schema to documents when standardizing. |
| `standardizeUsingSchema` | boolean | no | Whether to standardize the input documents using the newly created schema after generation.Note that standardizing documents costs credits just as if you had called the `/standardize` endpoint directly Default: `true`. |
| `standardizationMode` | list | no | *Advanced Feature* Mode of standardization to run, if standardizing using the schema. One of: `default`, `sectionBased`, `spatial`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "jobId": "string",
      "schemaId": "string",
      "schemaName": "Ava Chen",
      "standardizationIds": [
        "string"
      ],
      "standardizationJobIds": [
        "string"
      ],
      "status": "string"
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
| `standardizationIds` | array<string> | List of standardization IDs for the documents used to generate the schema. These will only become available after schema generation is complete, and only if standardizeUsingSchema is set to true. |
| `standardizationJobIds` | array<string> | List of standardization job IDs for the documents used to generate the schema. These will only become available after schema generation is complete, and only if standardizeUsingSchema is set to true. |
| `status` | string | Current status of the job. |

## Native endpoint

Through the native DocuPipe API, this operation is `POST /schema/autogenerate` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/auto-generate-a-schema.md) for the provider-specific parameters and requirements.

