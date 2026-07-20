# DocuPanda - Document Understanding: Add a New Schema

Creates a new schema in DocuPanda.

```
POST https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/post-schema
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPanda - Document Understanding `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/post-schema" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "jsonSchema": {},
  "schemaName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/post-schema', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "jsonSchema": {},
    "schemaName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `guidelines` | string | no | Guidelines to apply to the schema to documents when standardizing. |
| `jsonSchema` | object | yes | The new JSON schema to add. Must be a valid JSON schema (https://json-schema.org/). |
| `schemaName` | string | yes | Name of the new schema. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "jobId": "string",
      "schemaId": "string",
      "success": true,
      "timestamp": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `jobId` | string | Unique identifier of the job that made the schema. |
| `schemaId` | string | Unique identifier of the new schema. |
| `success` | boolean | Whether the schema was successfully added. |
| `timestamp` | string | Timestamp of the creation of the schema. |

## Native endpoint

Through the native DocuPanda - Document Understanding API, this operation is `POST /schema` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-schema.md) for the provider-specific parameters and requirements.

