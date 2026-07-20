# DocuPanda - Document Understanding: Copy a Schema to Another Workspace

Creates a schema copy in another DocuPanda workspace.

```
POST https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/post-copy-schema
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPanda - Document Understanding `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/post-copy-schema" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "schemaId": "string",
  "targetWorkspaceApiKey": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/post-copy-schema', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "schemaId": "string",
    "targetWorkspaceApiKey": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `schemaId` | string | yes | Unique identifier of the schema to copy. |
| `targetWorkspaceApiKey` | string | yes | API key of the target workspace to copy the schema to. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "guidelines": "string",
      "jsonSchema": {},
      "schemaId": "string",
      "schemaName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `guidelines` | string | Guidelines for the schema. |
| `jsonSchema` | object | The JSON schema that defines the structure of the data. |
| `schemaId` | string | Unique identifier of the schema. |
| `schemaName` | string | Name of the schema. |

## Native endpoint

Through the native DocuPanda - Document Understanding API, this operation is `POST /copy/schema` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-copy-schema.md) for the provider-specific parameters and requirements.

